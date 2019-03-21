---
layout: post
title: 'Git-hub Permission Error'
author: teddy
date: 2019-03-21 16:00
tags: [Git-hub]
image: /files/covers/head-tail.jpg
---

# Git-hub Push중 Permission Error
## 1. 증상
      Source Tree사용중 Push 중 아래와 같은 Error 메세지 표시
      Commend 명령에서도 같은 Error 메세지 표시
      하지만 Web에서는 다른 기능 사용 가능(Branch생성 또는 삭제) OWNER 권한
 ![Error Message](/files/posts/2019-03-21-1/1-1.png)
## 2. 해결 방안
### 1) 제어판에서 사용자 계정 선택
![방법 1](/files/posts/2019-03-21-1/1-2.png)
### 2) Windows 자격 증명 관리 선택
![방법 2](/files/posts/2019-03-21-1/1-3.png)
### 3) 일반 자격 증명 - Git-hub 선택
      자격증명 관리자 안에 일반 자격증명에 사이트마다 자격증명에 관한 데이터가 있습니다.
      그중에 git:https://github.com 에서 V를 눌러 세부 사항이 보이게 하고 편집을 선택합니다.
![방법 3](/files/posts/2019-03-21-1/1-4-1.png)
### 4) 일반 자격 증명 편집
      Git-hub에서 사용 중인 사용자 이름과 암호를 다시 입력 후 저장을 합니다.
![방법 4](/files/posts/2019-03-21-1/1-4.png)
### 4) Source Tree에서 사용 확인
      Source Tree나 Commend 입력 창에서 Push 사용 가능을 확인 할수 있습니다.
![방법 5](/files/posts/2019-03-21-1/1-6.png)
![방법 6](/files/posts/2019-03-21-1/1-5.png)
