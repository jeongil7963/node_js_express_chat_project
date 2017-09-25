# Nodejs의 socket을 이용하여 채팅구현

- socket의 양방향 통신을 이용하여 채팅을 구현한다.

## 사전 조건

- 서버 환경 : CentOS, NodeJS(express+socket.io)

## 구성하기

- 먼저, 서버에는 nodejs가 설치되어있어야 한다.

- 작업할 폴더를 생성한 후, 아래와 같이 package.json 파일을 생성한다.

- express 설치

## Server Application 작성

- node 서버를 돌리기 위해 소스와 같이 node_chat_server.js 를 작성한다.

## Socket.io 설치하기

- socket.io 를 설치

## Socket.io 사용하기

- socket.io 모듈을 불러와, connection 메세지를 받으면, 콘솔에 로그를 찍는 내용이다.

- 새로고침을 몇번 해보면, 'a user connected' 로그가 계속 찍힌다. 

- connect 와 disconnect가 언제 발생하는지 한번 살펴본다.

- 브라우저를 닫거나 새로고침하는순간 disconnect된다.

## 이벤트 전송

- input box에 메세지를 써놓고 전송버튼을 눌러, 서버로 메세지를 던진다.

- client side에서 socket 으로 'chat message' 이벤트를 보내면, 서버에서 받아서 console.log 에 출력하는 것이다.

## 브로드캐스팅

- 서버는 채팅 메세지를 받아서 모든 사용자에게 뿌려줄 것이다.

- 아래 소스와 같이 io.emit 한줄이 추가힌다.

- 서버에서 보냈으니, client side 에서도 받아서 표시한다.

- client side 에서도 마찬가지로 비동기로 처리된다.

- msg id를 가진 ul 에 li 를 append 하는 것이다.

- 브라우저에서 탭을 두개 열어 서로 채팅을 쳐본다.