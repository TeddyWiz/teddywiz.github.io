---
layout: post
title: 'Wifi Control Board 소개'
author: Teddy
date: 2019-03-06 09:00
tags: [WIZnet]
image: /files/covers/head-tail.jpg
---

# Wifi를 이용한 RGB LED Strips 및 Moter Control Board 소개
![Products](/files/posts/2019-03-06/Wifi_Control_Board.png)
## 1. 소개
 * 원본 사이트(https://www.elektor.com/wi-fi-controller-board-120718)

 * Wifi를 이용하여 웹서버 구성하여 RGB LED Strip을 제어 하는 제품입니다. 모터 제어도 가능합니다.
 * 사이트에서 조립된 보드 또는 PCB를 판매 하고 있습니다.
 또한 자신이 개발 중 격었던 에러 수정 내용등 을 PDF로 정리해 있어서 따라서 만들어 보기에 좋습니다.

## 2. 회로
 * 메인 MCU는 PIC18F14K50 입니다. 아두이노로 테스트 후에 적용 한 것같습니다.
 * Wifi는 WizFi220을 사용 하였습니다.
 * 전원은 Vin의 레귤레이터가 7~40V까지 연결가능합니다.

 ![Circuit](/files/posts/2019-03-06/Board_Circuit.png)

 ## 3. 프로그램
 * 테스트용 프로그램을 사이트에서 제공해 주고있습니다.
 * 웹서버를 구현해서 LAP(Limited Access Point) Mode를 이용해 Wifi 설정이 가능하게 했고 Wifi를 접속하여 Web 사이트에서 컨트롤이 가능하게 했습니다.
 * 프로그램 제공 사이트 (https://www.elektormagazine.com/magazine/elektor-201306/20740)

 ## 4. 동작 결과
 * LAP(Limited Access Point)mode에서 Wifi 설정 합니다.

 ![Web1](/files/posts/2019-03-06/web1.png)
 * 웹페이지에 접속하여 제어 합니다.

 ![Web2](/files/posts/2019-03-06/web2.png)
 * 아래 그림과 같이 동작 합니다.

 ![Result](/files/posts/2019-03-06/result.png)
 * 사이트에서 참고 하셔서 따라해보는 것도 즐거울 것 같습니다.
 감사합니다.
