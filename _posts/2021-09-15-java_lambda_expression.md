---
title: "[자바(JAVA)] 람다식(Lambda expression)"
categories:
- JAVA
tags: 
- [JAVA, Lambda expression]
date: 2021-09-15
last_modified_at: 2021-09-15
toc: true
toc_sticky: true
toc_label: "람다식"
---

## 람다식이란

자바 8부터 `함수형 프로그래밍` 방식을 지원하는데, 이를 람다식이라고 한다.

### 함수형 프로그래밍(FP)

함수형 프로그래밍(Functional Programming : FP)은 매개변수만을 사용하여 함수를 만들어 side effect가 나지 않도록 구현하는 방식이다.   
함수 내부에서 함수 외부에 있는 변수를 사용하지 않아 함수가 수행되더라도 외부에 영향을 주지 않는다.   
병렬 처리가 가능하다.

## 람다식 구현 방법

```java
( 매개변수 ) -> {실행문;}

(int x, int y) -> {return x+y;}
```

## 람다식의 특징

- 함수의 이름이 없다(= 익명함수다)
- 매개변수와 매개변수를 이용하여 실행한다
- 매개변수가 하나인 경우 자료형과 괄호 생략이 가능하다
- 매개변수가 두개 이상인 경우에는 생략이 불가능하다
- 실행문이 한문장인 경우 중괄호 생략이 가능하다
- return이 포함된 경우 중괄호 생략이 불가능하다.



