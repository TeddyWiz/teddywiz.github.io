---
layout: post
title: 'W6100EVB CubeMX 사용 Loopback test'
author: Teddy
date: 2019-03-21 19:00
tags: [Wiznet]
image: /files/covers/head-tail.jpg
---
<a id="forkme" href="https://github.com/Wiznet/W6100-EVB-Hal-TrueSTUDIO"></a>

# W6100EVB CubeMX 사용 Loopback test

## 1. CubeMX 설정 방법
 * CubeMX를 실행 후  File -> New Project를 클릭합니다.
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-00-1.png)

 * MCU chip 설정 후 더블클릭 합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-00-2.png)

 * 프로젝트가 생성이 된 후 아래와 같이 핀맵을 설정합니다. 통신 설정은 밑에 설명 합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-01.png)

 * RCC 설정에서 High Speed Clock을 Crystal/Ceramic Resonator로 설정합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-02.png)

 * Debug 설정 - Swdio를 쓰기 위하여 Serial Wire로 설정합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-03.png)

 * Uart 설정 - 디버그 및 통신 용도를 위하여 Asynchronous로 설정합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-04.png)

 * Uart 설정 - 메세지를 응답받을 때 인터럽르로 받기 위해 인터럽트 셋팅을 합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-05.png)

 * SPI 설정 - MODE를 Full-Duplex Master로 설정 합니다. NSS설정은 위의 GPIO 설정에서 합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-06.png)

 * Clock Configuration에서 아래와 같이 설정합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-07.png)

 * Project Manager에서 프로젝트 이름과 Toolchain 설정을 합니다. 저희는 TrueSTUDIO를 사용할 예정이라 TrueSTUDIO를 설정합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-08.png)

 * 설정을 완료 후에 GENERATE CODE를 클릭하여 코드를 생성합니다. 그리고 Open Project를 선택합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-09.png)

## 2. Driver file 다운로드 및 TrueSTUDIO 셋팅

 * Wiznet Git-Hub에서 Driver file을 다운받습니다. github site : [https://github.com/Wiznet/io6Library](https://github.com/Wiznet/io6Library).<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-10.png)

 * 다운 받은 파일을 생성한 프로젝트 폴더 안에 복사합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-11.png)

 * 다운 받은 파일 안에 Loopback 프로그램도 프로젝트 폴더 안에 복사합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-12.png)

 * 프로그램 프로젝트 폴더를 다른 위치에 복사해도 동작 시키기위해서 File Path를 설정해야 합니다.이전에 TrueSTUDIO의 프로젝트가 실행된 상태에서 왼쪽의 프로젝트명을 오른쪾 클릭하여 아래와 같이 나오면 특성을 클릭합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-13-1.png)

 * 창이 나오면 C/C++ Build에서 Environment를 클릭합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-13-2.png)

 * Add를 눌러 나오는 창에 Name에 PROJECT, Value에 ${ProjDirPath}를 넣습니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-13.png)

 * C/C++ Geneal에서 Paths and Symbol에서 아래와 같이 입력합니다. 그리고 아까 추가했던 Driver File을 적용하기위해 File Path 하나를 더 추가 합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-14.png)

## 3. LoopBack 프로그램

 * Driver 코드와 Loopback 프로그램을 가져오기 위해서 아래와 같이 입력합니다.
 * 코드입력은 왼쪽의 숫자와 각각의 생성된 주석을 참고 하여 입력합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-16.png)

 * 왼쪽 프로젝트 탐색기에서 Src폴더 안에 main.c 파일을 열어서 아래와 같이 입력합니다.
 * 아래 코드는 _ write()함수는 uart를 printf로 쓰기위해서 필요합니다.<br>
 * HAL_UART_RxCpltCallback()함수는 Uart응답 받았을 때 인터럽트에서 처리하는 코드를 넣어주기 위해 필요 합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-15.png)


 * MAC과 IP등 설정을 입력합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-18.png)

 * W6100 Initialize를 위한 함수를 입력합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-19.png)

 * Main 함수에서 설정 함수와 Initialize 함수를 호출 하고 Loopback 프로그램을 입력합니다..<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-20.png)

 * 입력이 끝나면 위쪽의 도구모음에 망치 모양을 클릭하여  Build하고 풍댕이 모양의 debug를 클릭합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-22.png)

 * Hercules 프로그램을 이용하여 구동하는 것을 확인합니다.<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-23.png)

 * TCP Client에서 Loopback 메세지가 실행 되는 것을 확인합니다..<br>
 ![setting](/files/posts/2019-03-21-2/2019-03-21-2-24.png)

감사합니다.
