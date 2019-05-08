---
layout: post
title: 'CubeMX Generated Project Keil setting'
author: Teddy
date: 2019-05-08 09:00
tags: [Wiznet]
image: /files/covers/head-tail.jpg
---

# CubeMX Generated Project Keil setting

## Project file 추가

### 1. 프로젝트 폴더에서 오른쪽 클릭 Manage Project Items 버튼 선택
 - 왼쪽의 파일들 추가

<p align="center">
  <img width="60%" src="files\posts\2019-05-08-1\20190508_1_001.png" />
</p>

### 2. Goups 선택 후 파일 추가

<p align="center">
  <img width="60%" src="..\files\posts\2019-05-08-1\20190508_1_002.png" />
</p>

## Project Setting

### 1. 프로젝트 폴더에서 오른쪽 클릭 Options for Target ... 선택

<p align="center">
  <img width="60%" src="..\files\posts\2019-05-08-1\20190508_1_003.png" />
</p>

### 2. Target에서 Use MicroLIB 체크 확인
 - 여기 체크 안되면 Printf 사용 불가

<p align="center">
  <img width="60%" src="..\files\posts\2019-05-08-1\20190508_1_004.png" />
</p>

### 3. Include Paths 버튼 클릭

<p align="center">
  <img width="60%" src="..\files\posts\2019-05-08-1\20190508_1_005.png" />
</p>

### 4. Folder Setup에서 파일 경로 추가
 - 빈칸 클릭 후 1번 선택 2번에 경로 기입 후 3번 OK 버튼으로 완료

<p align="center">
  <img width="60%" src="..\files\posts\2019-05-08-1\20190508_1_006.png" />
</p>

## Printf 사용 구문 추가
- 꼭 USER CODE BEGIN 과 END 사이에 추가하세요
- 아니면 CubeMX 재생성하면 없어집니다.
<p align="center">
  <img width="60%" src="..\files\posts\2019-05-08-1\20190508_1_007.png" />
</p>

이렇게 설정하시고 사용 하시면 됩니다