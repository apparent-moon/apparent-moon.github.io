---
title: "[자바(JAVA)] Get, Set 메소드 (getter, setter)"
categories:
- JAVA
tags: 
- [JAVA, Getter, Setter]
date: 2021-08-18
last_modified_at: 2021-08-18
toc: true
toc_sticky: true
toc_label: "Get Set 메소드"
---

## Getter Setter의 역할, 이유

getter setter는 변수에 private 접근 연산자를 사용할 경우 외부에서 접근이 불가능하므로, 외부에서 접근을 할 수 있도록 해주는 메소드다.

객체 지향 프로그래밍에서는 **무결성**을 지키기 위해서 객체 외부에서 직접적으로 접근하는것을 좋아하지 않는다.   
그래서 무결성을 지키기 위해 메소드를 통해서 필드에 접근하도록 유도하는 방식이, getter setter 를 이용하는 이유다!

무결성: 양수값만 받아야하는데 그 값을 음수로 바꾸는 행위와 같이, 프로그램에서 원하지 않는 방향으로 외부에서 수정하는 행위(=결점)가 발생하도록 하는것

## 언제 사용할까?

필드가 **private** 접근 제한자를 가지고 있을 때 사용한다!

### get 메소드 (getter)

값을 반환하는것이 목적인 메소드로 return값이 반드시 있어야 한다.   
필드의 값을 외부로 리턴해줄 때   
즉, 외부에서 객체의 데이터를 __읽을 때__ 사용한다.

### set 메소드 (setter)

값을 할당하는것이 목적인 메소드.   
외부에서 객체에 값을 변경할 때 사용한다.

### 외부에서 값 읽기만 허용하고싶을때는?!

1. setter를 선언하지 않고, getter만 선언한다.
2. setter에 private 접근제한자를 붙인다.