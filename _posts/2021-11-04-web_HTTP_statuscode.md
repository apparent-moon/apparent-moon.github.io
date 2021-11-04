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

## HTTP 상태코드

클라이언트가 보낸 요청의 처리 상태를 응답에서 알려주는 기능

### 1xx (Informational)

요청 처리 중

### 2xx (Successful)

요청 정상 처리

#### 200 OK

클라이언트에서 요청한 리소스를 서버에서 정상적으로 처리하여 응답한 상태

#### 201 Created

요청을 성공하여 새로운 리소스가 생성됨

- POST방식으로 새로운 리소스 생성을 요청을 하였을 때, 서버에서 정상적으로 처리하여, HTTP Response Location 헤더 필드로 식별

#### 202 Accepted

요청이 접수되었으나 처리가 완료되지 않음   
다른 프로세스에서 처리 또는 서버가 요청을 다루고 있거나 배치 프로세스를 하고 있는 경우에 사용된다

- 배치

#### 204 NO Content

서버가 요청을 성공적으로 수행했지만, 응답 페이로드 본문에 보낼 데이터가 없음

### 3xx (Redirection)

요청을 완료하려면 추가 행동이 필요함

### 4xx (Client Error)

클라이언트 오류

### 5xx (Server Error)

서버 오류
