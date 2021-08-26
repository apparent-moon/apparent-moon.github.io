---
title: "[자바(JAVA)] 추상(abstract)"
categories:
- JAVA
tags: 
- [JAVA, Abstract]
date: 2021-08-26
last_modified_at: 2021-08-26
toc: true
toc_sticky: true
toc_label: "추상(abstract)"
---

## 추상(abstract) 클래스

구현 코드 없이 메소드의 선언만 있는 `추상 메소드`를 포함한 클래스.(추상메소드가 반드시 포함되어야 하는것은 아닌것 같지만, 추상클래스를 사용하다보면 추상메소드도 같이 사용하게 된다.)   
객체를 직접 생성할 수 없다.(↔ 실체클래스 : 객체를 직접 생성할 수 있는 클래스)   
하지만 클래스들의 공통적인 특성(필드, 메소드)들이 선언되어 있다.
그래서, 추상클래스가 부모클래스이고 실체클래스가 자식클래스로 구현할 수 있다.


### 추상 클래스 선언 방법

`abstract` 예약어를 사용한다.

```java
public abstract class 클래스명{

}
```

추상 클래스를 이용하는 **자식클래스(실체클래스)**는 이렇게 사용한다
```java
public class 클래스명 extends 추상클래스명{
    
}
```


## 추상(abstract) 메소드

추상메소드는 추상 클래스에 선언된 메소드를 말한다. 메소드가 구현/정의 된 경우에는 추상 메소드가 아니다!

### 메소드 선언과 정의의 차이
>메소드 선언 : 반환타입, 메서드 이름, 매개변수로 구성된다

```java
int turnOn(int x);
```

>메소드 정의(=메소드 구현) : 구현부(body)를 가진다.

```java
int turnOff(int y){
// { } 중괄호 안이 구현부이다. 즉 {   } 중괄호를 포함하면 메소드 정의!
}
```

### 추상 메소드 선언 방법

추상 메소드는 `abstract` 예약어를 포함하여 작성한다.

```java
public abstract class 추상클래스명 {
    public abstract 리턴타입 메소드명();
}
```

### 추상 메소드 선언 이유

1. 추상 클래스는 하위 클래스에서 공통적으로 사용하는 특성을 포함하는데,하위클래스들이 같은 이름으로 된 메소드를 다른 내용으로 사용을 해야할 수도 있으므로 이를 위해서 추상 메소드를 선언한다.   
2. 반드시 하위 클래스에서 해당 메소드를 사용해야 한다고 정의하고 싶을 때 추상 메소드로 선언한다.

*** 
> Animal.java

```java
public abstract class Animal {
    public abstract void Sound();
}
```
예를들어, Animal 이름의 추상클래스가 Dog, Cat 을 하위클래스로 가질 때, Dog와 Cat의 울음소리를 다르게 출력하기 위해서 Sound 메소드를 추상메소드로 선언할 수 있다.

### 하위 클래스에서 추상메소드 재정의 방법

```java
{
public class 하위클래스명 extends 추상클래스명{
...
@Override
//여기에 추상 클래스의 추상메소드를 재정의한다. @Override 어노테이션이 필요하다!
}
```