---
title: "[네트워크] URI URL URN"
categories:
- Network
tags: 
- [Network, Computer Network, URI, URL, URN]
date: 2021-10-29
last_modified_at: 2021-10-29
toc: true
toc_sticky: true
toc_label: "URI URL URN"
---

## URI(Uniform Resource Identifier) : 통합 자원 식별자

- 자원(인터넷 상의 리소스)을 구분하고 접근하기 위해 사용하는 유일한 식별자.
- 실제 존재할 수 있는/존재하지 않는 파일 또는 자원의 위치를 나타낸다
- URI의 하위개념으로 `URI`와 `URN`이 포함되어있다


## URL(Uniform Resource Locator) : 통합 자원 위치

- 자원의 위치에 대한 경로값(위치값)을 지닌 문자열
- 자원(리소스)의 구체적인 위치를 서술한 문자열
- http:// , https:// 등의 프로토콜을 이용한다

## URN(Uniform Resource Name) : 통합 자원 이름

- 자원의 이름을 나타낸다
- 프로토콜을 포함하지 않는다
- urn:scheme를 사용한다
- 영속적이고 독립적인 자원을 위한 지시자

## URL과 URN의 차이점

http://gahyeon.moon/a/bb/ccc 이런 URL이 특정한 파일을 나타낼 때, http://gahyeon.moon/a/bb/dddd 로 바뀌면 다른 파일의 위치를 나타낸다.

하지만 특정 파일의 urn이 `urn:ccc` 라면 파일의 위치가 바뀌어도 `urn:ccc`를 클릭하면 특정 파일의 호출이 가능하다.

(실제로 urn이 이런 주소는 아니지만? 이해하기 편하기 위해서 이렇게 설명함.)