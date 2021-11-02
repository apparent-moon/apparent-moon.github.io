---
title: "[네트워크] TCP와 UDP"
categories:
- Network
tags: 
- [Network, Computer Network, TCP, UDP]
date: 2021-11-02
last_modified_at: 2021-11-02
toc: true
toc_sticky: true
toc_label: "TCP & UDP"
---

## TCP(Transmisiion Control Protocol) : 전송 제어 프로토콜

- IP와 함께 TCP/IP라는 명칭으로 사용된다.

### 특징

1. 신뢰성 보장
2. 연결 지향적 특징 (TCP 3-way handshaking으로 연결 설정) : 목적지와 수신지를 확실히 함
3. 흐름제어
4. 혼잡제어

### 패킷(Packet = Package + Bucket)

### TCP 3-way handshaking

1. 클라이언트 -> 서버 | SYN : 접속 요청
2. 서버 -> 클라이언트 | ACK : 요청 수락 + SYN : 접속 요청
3. 클라이언트 -> 서버 | ACK | (이때 데이터 전송하기도 함)
4. 데이터 전송

## UDP(User Datagram Protocol) : 사용자 데이터그램 프로토콜

- 전송계층(OSI 4계층)의 통신 프로토콜

### 특징

1. 비연결형 서비스(연결설정이 없다)
2. 비신뢰성
3. 데이터를 `데이터그램` 단위로 처리함
> 데이터그램 : 독립적인 관계를 지니는 패킷
4. 순서화되지 않은 데이터그램 서비스 제공
5. 단순하고 빠른속도를 가짐
6. 스트리밍 서비스에 자주 사용함.
7. 멀티캐스팅이 가능하여 여러 다수 지점에 전송이 가능함.

|특징|TCP|UDP|
|-|-|-|
|속도|느리다|빠르다|
|신뢰성|신뢰성 보장O| 신뢰성 보장X|
|연결| 연결형 서비스 | 비연결형 서비스|
|전송순서| 전송순서를 보장함 | 전송순서를 보장하지 않음|
|통신 방식 | 1:1 | 1:n |