# arduino_iot

## 프로젝트 목표

- 하드웨어, 웹 서버, DB, IOT의 이해와 MQTT 방식으로 하드웨어와 소프트웨어의 통신이 가능캐끔 하는 것
- 통신한 정보를 DB에 저장하고 활용할 수 있게 하는 것

## 사용 IDE

1. Arduino IDE
2. Visual Studio Code

## 사용 언어 / 어플리케이션

1. Nodejs (Express) - 벡엔드 API 구축을 위함

2. NginX - 웹 서버 구축을 위함

3. Arduino - 하드웨어의 컨트롤을 위함

4. SQL (Maria DB) - 하드웨어로부터 정보를 저장하기 위함

5. BootStrap - 빠르고 간단한 프론트엔드 디자인을 위함

## 통신 방법

1. 하드웨어와 클라우드 서버

  - 원래 하드웨어와 클라우드의 통신을 통하여 PUB-SUB관계의 MQTT 통신을 하려 의도.
  - 하드웨어 상의 문제로 SERIAL PORT통신으로 Node로 보내고, 그 노드가 AWS IOT 클라우드로 PUB-SUB 관계를 가진다.

2. 클라우드 서버와 웹, DB 서버

  - 하드웨어에서 클라우드 서버와 또다른 클라우드 서버를 통해서 Publish된 정보들을 DB에 저장
  - DB의 저장한 데이터들을 REST API 형식으로 프론트 엔드로 전달한다.
