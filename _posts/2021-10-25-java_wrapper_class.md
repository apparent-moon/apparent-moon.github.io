---
title: "[자바(JAVA)] 래퍼클래스(Wrapper class)"
categories:
- JAVA
tags: 
- [JAVA, Wrapper class]
date: 2021-10-25
last_modified_at: 2021-10-25
toc: true
toc_sticky: true
toc_label: "래퍼클래스(Wrapper class)"
---

## 래퍼 클래스(wrapper class)

기본 자료형을 **객체**로 다루기 위한 클래스

|기본형|래퍼클래스|
|--|--|
|byte|Byte|
|char|Character|
|int|Integer|
|float|Float|
|double|Double|
|long|Long|
|short|Short|
|boolean|Boolean|

## 특징

1. 모든 래퍼 클래스의 부모는 Object 클래스다.
2. 문자열을 기본 타입값으로 변환할 때 사용한다.

```java
String num = "10"

Integer Inum = Integer.parseInt(num); //산술연산이 *가능*한 10이 나옴.(int형으로 반환)

Integer Inum2 = Integer.valueOf(num); //산술연산이 *불가능*한 10이 나옴.(Integer형으로 반환)
```
3. **equals**를 이용하여 객체 값을 비교해야한다.
4. null값 처리가 용이하다.

## Boxing & UnBoxing
### Boxing

기본형 -> 래퍼클래스

### UnBoxing

래퍼클래스 -> 기본형