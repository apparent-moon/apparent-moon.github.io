---
title: "[자바(JAVA)] 예외처리"
categories:
- JAVA
tags: 
- [JAVA, ]
date: 2021-09-07
last_modified_at: 2021-09-08
toc: true
toc_sticky: true
toc_label: "예외처리"
---

## 오류와 예외

오류(error) : 가상 머신에서 발생하여 프로그래머가 처리할 수 없는 오류   
예외(exception) : 프로그램에서 제어할 수 있는 오류

### 컴파일 오류

프로그램 코드 작성 중 발생하는 문법적 오류

### 실행 오류

실행 중인 프로그램이 의도하지 않은 동작을 하거나 프로그램이 중지되는 오류

## 예외클래스

모든 예외 클래스는 `java.lang.Exception` 클래스를 상속받는다.

[Object class](https://docs.oracle.com/javase/7/docs/api/java/lang/Exception.html)

## 예외 처리하기

프로그램의 비정상적인 종료를 막고 정상적인 실행상태를 유지하기 위해서 예외처리를 해야한다.

* * *

### 예외 복구

> 에러가 발생했을 때, 다른 작업 흐름으로 유도하는 것

> try-catch문

```java
try{
    예외 발생 가능 코드
}catch(예외클래스 e){
    예외 처리(try문에서 예외가 발생했을 경우 catch문 안에서 처리한다)
}
```

> try-catch-finally 문

`finally` 블록은 생략하고 `try-catch`로만 작성해도 상관없다.

finally문에서는 파일을 닫거나 네트워크를 닫는 등 리소스 해제 구현을 주로 한다.

```java
try{
    예외 발생 가능 코드
}catch(예외클래스 e){
    예외 처리(try문에서 예외가 발생했을 경우 catch문 안에서 처리한다)
}finally{
    예외 발생 여부와 상관없이 항상 실행 코드
}
```

### 예외처리 회피

> 예외처리 회피 : 처리하지 않고 호출한쪽으로 throw

1. throws를 선언
2. catch로 예외를 잡고, 다시 예외를 잡는 방법

```java
public void method() throws Exception{
    try{

    } catch() {
        throw e
    }
}
```

### 예외 전환

> 예외전환 : 발생한 예외를 상황에 맞는 적절한 예외로 전환해서 던지는 방법


### 다중 예외 처리

try문안에서 2개 이상의 에러가 발생할경우에는 catch문을 2개 사용하여 예외 처리를 해준다.

```java
try{
    에러1 코드;
    에러2 코드;
}catch(에러1예외처리 e){

}catch(에러2예외처리 e){

}
```

- 상위 예외 클래스가 하위예외 클래스보다 아래쪽에 위치해야한다.

### 사용자 정의 예외처리(고의로 예외 발생시키기)

> 직접 사용자정의 예외를 발생시킬 때 사용한다.

new 연산자를 이용하여 예외 클래스의 객체를 만들고 `throw`를 이용해서 예외를 발생시킨다.

```java
try{
    Exception e = new Exception("이렇게 직접 고의로 발생시킨다");
}catch(Exception e){

}
```

* * *
## Runtime Exception(실행 오류 예외 처리)

### ArithmeticException

정수를 0으로 나눌 때 발생   
[공식문서 링크](https://docs.oracle.com/javase/7/docs/api/java/lang/ArithmeticException.html)

### NullPointerException

객체가 없는 상태에서 객체를 사용하려고 할 때 발생   
[공식문서 링크](https://docs.oracle.com/javase/7/docs/api/java/lang/NullPointerException.html)

### ArrayIndexOutOfBoundsException

배열에서 인덱스 범위를 초과할 경우 발생   
[공식문서 링크](https://docs.oracle.com/javase/7/docs/api/java/lang/ArrayIndexOutOfBoundsException.html)

### NumberFormatException

문자열을 정수로 변환하거나 실수로 변환할 때, 변환될 수 없는 문자가 포함되어 있을 때 발생   
[공식문서 링크](https://docs.oracle.com/javase/8/docs/api/java/lang/NumberFormatException.html)

### ClassCastException

추상클래스나 구현클래스에서, 상속관계가 아닌 다른 타입으로 클래스 변환 시 발생   
[공식문서 링크](https://docs.oracle.com/javase/8/docs/api/java/lang/ClassCastException.html)

## IO Exception(입출력 예외 처리)

### FileNotFoundException

파일이 없는 경우 발생   
[공식문서 링크](https://docs.oracle.com/javase/8/docs/api/java/io/FileNotFoundException.html)

### SocketException

소켓을 만들거나 접근하는 과정에서 오류가 발생하였을 경우 사용   
[공식문서 링크](https://docs.oracle.com/javase/8/docs/api/java/net/SocketException.html)






