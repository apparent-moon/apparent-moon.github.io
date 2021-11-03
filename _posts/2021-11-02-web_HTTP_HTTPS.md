---
title: "[네트워크] HTTP 와 HTTPS"
categories:
- Network
tags: 
- [Network, Computer Network, HTTP, HTTPS]
date: 2021-11-03
last_modified_at: 2021-11-03
toc: true
toc_sticky: true
toc_label: "HTTP"
---

## HTTP (HyperText Transfer Porocol)



### 특징
- 클라이언트-서버 구조 (Request Response)
    + 클라이언트는 서버에 요청을 보내고 응답을 대기한다
    + 서버가 요청에 대한 결과를 만들어서 응답한다
- 무상태 프로토콜 지향(Stateless)
    + 응답 서버를 쉽게 바꿀 수 있다
- 비연결성
- HTTP 메시지를 통해서 통신
- 단순하고 확장이 가능하다
- 기본포트로 80번을 사용한다

## HTTPS (HyperText Transfer Protocol Secure)

데이터를 전송하기 전 내용을 `암호화` 한다

### 특징

- 기밀성
- 무결성
- 인증
- 기본포트로 443번을 사용한다.
