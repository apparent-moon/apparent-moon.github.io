---
title: "[자바(JAVA)] Stack"
categories:
- JAVA
tags: 
- [JAVA, Stack]
date: 2021-09-29
last_modified_at: 2021-09-29
toc: true
toc_sticky: true
toc_label: "Stack"
---

## Stack

- LIFO(Last In First Out) 의 형태를 가진 자료구조

## Stack 선언 방법

```java
Stack<자료형> 변수명 = new Stack<>();

[ex]
Stack<Integer> stack = new Stack<>();
```

## Stack 메소드

### push()

stack에 데이터를 추가해준다

```java
변수명.push(데이터);

[ex]
Stack<Integer> stack = new Stack<>();
stack.push(1); //stack에 1을 추가함
```

### pop()

스택에 추가된 최근 데이터를 삭제한다

```java
변수명.pop();

[ex]
Stack<Integer> stack = new Stack<>();
stack.push(1); //stack에 1을 추가함
stack.pop(); //최근에 추가된 1을 삭제함.
```

### peek()

스택에 추가된 최근 데이터를 조회한다

```java
변수명.peek()

[ex]
Stack<Integer> stack = new Stack<>();
stack.push(1)
stack.peek(); // 최근에 추가된 1을 검색해서 반환해준다.
```

### isEmpty();

스택이 빈값인지 체크헤서 t/f를 반환한다.
