---
layout: post
title: 'W5x00 Integration Project Tutorial'
author: Teddy
date: 2020-02-06 17:40
tags: [Wiznet]
image: /files/covers/head-tail.jpg
---

# W5x00 Integration Project Tutorial in True studio

## Hardware configuration
test
![WizFi360 Arduino link](/files/arduino/w600-arduino-0.2.7-rc1.zip)
### System Diagram
- ST-link connect to W5100s-EVB
- W5100s-EVB SPI connect to WIZ850io, WIZ820io, WIZ810io
- Total Diagram

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_001.png?raw=true" />
</p>

- W5100s-EVB PIN MAP

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_002.png?raw=true" />
</p>

- WIZ850io PIN MAP

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_003.png?raw=true" />
</p>

- - WIZ810io PIN MAP

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_004.png?raw=true" />
</p>

- WIZ820io PIN MAP

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_005.png?raw=true" />
</p>

- WIZ811MJ PIN MAP

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_006.png?raw=true" />
</p>

### Project Git-Hub Repository

- Connect to https://github.com/WIZnet-ioLibrary/W5x00_Loopback_with_W5100S_EVB

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_007.png?raw=true" />
</p>

- download Project File or Git-Hub Clone

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_008.png?raw=true" />
</p>

### Run True studio
- Set address for Workspace

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_009.png?raw=true" />
</p>

- First Program view

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_010.png?raw=true" />
</p>

### Open project

- Click MENU - File - Open Project from File System 

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_011.png?raw=true" />
</p>

- Click Directory Button for find Project file

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_012.png?raw=true" />
</p>

- Find Project Folder and Click "OK" button

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_013.png?raw=true" />
</p>

- Check Import Project and Click "Finish" button

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_014.png?raw=true" />
</p>

- Find wizchip_conf.h in Project Explorer and open file

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_015.png?raw=true" />
</p>

- Modify  _WIZCHIP_ value into set Chip name 
- This example the chip name is W5100S

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_016.png?raw=true" />
</p>

- Check to define "SPI_Arduino" for using SPI1 in HAL_Conifg.h

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_017.png?raw=true" />
</p>

- Build the project be clicked on the icon in the red square box and will be raised bar gage of build.

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_018.png?raw=true" />
</p>

- This window displays the result of the build.

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_019.png?raw=true" />
</p>

- Result of the running the program.

<p align="center">
  <img width="60%" src="https://github.com/TeddyWiz/teddywiz.github.io/blob/master/files/posts/2020-02-06-1/W5x00_IntegrationProject_020.png?raw=true" />
</p>
