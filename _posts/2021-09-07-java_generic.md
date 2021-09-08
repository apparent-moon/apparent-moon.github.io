---
title: "[자바(JAVA)] Object클래스"
categories:
- JAVA
tags: 
- [JAVA, Object class, java.lang]
date: 2021-09-06
last_modified_at: 2021-09-06
toc: true
toc_sticky: true
toc_label: "Object class"
---

## Generic 자료형

클래스의 자료형을 특정하지 않고 추후 해당 클래스를 사용할 때 지정할 수 있도록 선언하는 방식.

자료형의 변환은 컴파일러에 의해서 검증된다.

컬렉션 프레임워크에서 많이 사용되고있다.

### 자료형 매개변수(Type parameter)

이 클래스를 사용하는 시점에 실제 사용할 자료형을 지정, static변수는 사용할 수 없다.

- E : Element
- K : Key
- V : Value
- N : Number
- T : Type

### 다이아몬드 연산자 <>

다이아몬드 연산자 내부에서 자료형은 생략이 가능하다.

### Generic 메소드

자료형 매개변수를 베소드의 매개변수나 반환값으로 가지는 메소드.

```java
public <자료형 매개변수> 반환형 메소드명(자료형 매개변수){

}
```

