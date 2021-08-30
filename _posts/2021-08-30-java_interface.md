---
title: "[자바(JAVA)] 인터페이스(interface)"
categories:
- JAVA
tags: 
- [JAVA, Interface]
date: 2021-08-30
last_modified_at: 2021-08-30
toc: true
toc_sticky: true
toc_label: "인터페이스(interface)"
---

## 인터페이스(interface)

인터페이스는 객체의 사용 방법을 명세한 타입이다.   
사용자는 인터페이스의 메소드만 알고있으면 객체 내부가 바뀌어도 인터페이스를 통해 동일한 방법으로 사용이 가능하다.

## 인터페이스 선언 방법

```java
public interface 인터페이스변수명{

//상수

//추상 메소드

}
```
인터페이스는 객체로 생성할 수 없기 때문에, 생성자를 가질 수없다

### 상수
* 인터페이스는 `객체 사용방법`을 정의하는 역할을 하므로, 인스턴스 또는 정적필드 선언이 불가능하다.(=인터페이스를 통해 데이터를 저장하거나, 변하는 값은 선언이 불가하다.)
* 상수는 선언이 가능하지만, 실행시 **데이터 변경이 불가능**하다.
* 인터페이스에 선언 된 상수는 모두 `public static final`의 특성을 가져서 생략하더라도 **컴파일 과정에서 자동**으로 처리된다.
* 상수 이름은 대문자와 (_) 언더바를 이용해서 작성한다.

```java
public interface RemoteControl{
    public static final int MAX_VOLUME = 100;
    int MIN_VOLUME = 0; //컴파일 과정에서 자동으로 public static final 키워드(=예약어)가 처리된다.
}
```

### 추상 메소드(abstract)
* 추상 메소드는 중괄호({ }) 즉 구현부가 없는 메소드를 말한다.
* 인터페이스에 선언 된 추상메소드는 `public abstract`의 특성을 가져서 생략하더라도 **컴파일 과정에서 자동**으로 처리된다.

```java
public interface RemoteControl{
    public abstract void turnOn();
    void turnOff(); //컴파일 과정에서 public abstract 키워드(=예약어)가 처리된다.
}
```

### default 메소드(java8 이상)

인터페이스 내부에 구현하는 메소드로, 구현 클래스에서 공통으로 사용할 수 있는 기본 메소드

```java
default void Introduction(){
    System.out.println("소개합니다");
}
```

### static 메소드

인스턴스 생성과 상관 없이 인터페이스 타입으로 사용할 수 있는 메소드

```java
static int toal(int num){
    return num+num;
}
```

### private 메소드(java9 이상)

* default메소드나 static 메소드에서 사용함
* 인터페이스를 구현한 구현클래스에서는 사용하거나 재정의가 불가함
* 인터페이스 내부에서만 사용하기 위해 구현하는 메소드

## 인터페이스 구현
인터페이스 메소드를 통해 만드는 객체를 **구현객체**   
구현 객체를 생성하는 클래스를 **구현클래스**

### 구현 클래스

* `implements` 키워드를 통해서 클래스를 생성한다.
* 인터페이스가 `public` 접근 제한을 가지므로, 구현 클래스에서 `public` 접근제한자보다 낮은 제한은 작성할 수 없다.

```java
public class 구현클래스명 implements 인터페이스명{

    //인터페이스의 추상메소드를 실체메소드로 선언

}
```

인터페이스는 다중으로 선언이 가능하다.

```java
public class 구현클래스명 implements 인터페이스명1, 인터페이스명2 ... {

    //인터페이스1의 실체메소드

    //인터페이스2의 실체메소드

}
```

* 다중으로 선언할 때, 인터페이스들에 동일한 이름의 default 메소드가 선언되어있다면 둘 중 하나의 default 메소드를 재정의(overriding)하여 모호성을 없애야한다.

## 인터페이스간의 상속

* `extends` 키워드를 사용하여 인터페이스 간에 상속이 가능하다!   

```java

public interface 인터페이스변수명 extends 상위인터페이스(?)명{

}

[EX]
public interface ExtendsInterface extends X, Y{
    void hello();
}
```