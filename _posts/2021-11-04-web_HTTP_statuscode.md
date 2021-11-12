---
title: "[웹] HTTP 상태 코드"
categories:
- Network
tags: 
- [Web, HTTP]
date: 2021-11-04
last_modified_at: 2021-11-04
toc: true
toc_sticky: true
toc_label: "HTTP 상태 코드"
---

# HTTP 상태코드

클라이언트가 보낸 요청의 처리 상태를 응답에서 알려주는 기능

## 1xx (Informational)

요청 처리 중

## 2xx (Successful)

요청 정상 처리

### 200 OK

클라이언트에서 요청한 리소스를 서버에서 정상적으로 처리하여 응답한 상태

### 201 Created

요청을 성공하여 새로운 리소스가 생성됨

- POST방식으로 새로운 리소스 생성을 요청을 하였을 때, 서버에서 정상적으로 처리하여, HTTP Response Location 헤더 필드로 식별

### 202 Accepted

요청이 접수되었으나 처리가 완료되지 않음   
다른 프로세스에서 처리 또는 서버가 요청을 다루고 있거나 배치 프로세스를 하고 있는 경우에 사용된다

- 배치

### 204 NO Content

서버가 요청을 성공적으로 수행했지만, 응답 페이로드 본문에 보낼 데이터가 없음

## 3xx (Redirection)

요청을 완료하려면 추가 행동이 필요함.

### 리다이렉션

결과에 Location 헤더가 있으면, Location 위치로 이동하는것

- 영구 리다이렉션
    + 특정 리소스의 URI가 영구적으로 이동
- 일시 리다이렉션
    + 일시적인 변경(ex. 주문 완료 후 주문 내역 화면으로 이동)
- 특수 리다이렉션
    + 결과 대신 캐시를 사용함

### 300 Multiple Choices

### 301 Moved Permanently

리소스의 URI가 영구적으로 이동한것을 알려줌
리다이렉트시 요청 메소드가 GET으로 변하고, 본문이 제거될 수 있음

### 302 Found

리다이렉트시 요청 메소드가 GET으로 변하고, 본문이 제거될 수 있음

### 303 See Other

리다이렉트시 요청 메소드가 GET으로 변경

### 304 Not Modified

캐시를 목적으로 사용   
캐시로 리다이렉트.

### 307 Temporary Redirect

리다이렉트시 요청 메소드와 본문 유지

### 308 Permanent Redirect

리다이렉트시 요청 메소드와 본문을 유지함.(301과 다르게 메소드가 변하지 않는다.)   
-> 308보다는 301을 더 많이 사용함 

## 4xx (Client Error)

클라이언트 오류

### 400 Bad Request

클라이언트가 잘못된 요청을 해서 서버가 요청을 처리할 수 없음.

### 401 Unauthorized

클라이언트가 해당 리소스에 대한 인증이 필요함.   
-> 로그인 오류

### 403 Forbidden

서버가 요청을 이해햇지만 승인을 거부함.   
-> 접근권한이 불충분한 경우.

### 404 Not Found

요청 리소스를 찾을 수 없음.

## 5xx (Server Error)

서버 오류
-> 재시도시 성공할 수 있다(복구가 된 경우에!)

### 500 Internal Server Error

서버 문제로 오류 발생

### 503 Service Unavailable

서버스 이용 불가   
-> 서버의 일시적인 과부하 또는 예정된 작업(점검등...)으로 요청을 처리할 수 없는 경우
