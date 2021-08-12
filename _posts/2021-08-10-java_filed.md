---
title: "[자바(JAVA)] 필드(filed) (=전역변수, 멤버변수)"
categories:
- JAVA
tags: 
- [JAVA, field]
date: 2021-08-12
last_modified_at: 2021-08-12
toc: true
toc_sticky: true
toc_label: "필드(=전역변수,멤버변수)"
---

## 필드(filed)

필드는 객체의 데이터를 저장하는 곳으로, 객체가 가지는 속성을 변수로 표현한 것이다.

만약 Student 라는 클래스의 필드로는 학번,이름 등이 필드로 선언될 수 있겠다!

## 필드의 동의어

강의를 듣고 책으로 공부하다보면 똑같은 역할을 하는데 다양한 단어로 불린다.

나중에 헷갈리지 않게 공부하면서 기억하고 갈것!!!

필드는 **전역변수** 와 **멤버변수** 로도 불린다
{: .notice--success}

### 필드 위치

필드는 클래스 중괄호 {} 블록 어디에든 선언이 가능하다.

생성자와 메소드 안에는 선언하면 더이상 필드가 아니다.   
지역변수가 되어버린다.

>Car.java

```java
public class Car {
    //carNumber, carName이 필드!
	int carNumber;
	String carName = "붕붕이";

    //turnOn, turnOff는 메소드! 메소드 안에는 넣으면 필드가 아님!
    void turnOn() {
	    System.out.println("시동을 켭니다.");
	}

    void turnOff(){
        System.out.println("시동을 끕니다.")
    }

    //Car() 이건 생성자! 생성자 안에는 넣으면 필드가 아님!
    Car(){

    }
}
```

위의 코드에서 필드(=전역변수=멤버변수)는 `carNumber`와 `carName`이다!


### 필드 형태

```
1. 타입 변수명;
2. 타입 변수명 = 초기값;
```

위의 두가지 형태 다 가능한데, _초기값을 설정해주지 않은 경우에는_ **기본 초기값**이 설정된다.

### 초기값

| 타입 | 초기값 |
|--|--|
| byte | 0 |
| char | \u0000 |
| short | 0 |
| int | 0 |
| long | 0L |
| float | 0.0F |
| double | 0.0 |
| boolean | false |
| 배열 | null |
| 클래스 | null |
| 인터페이스 | null |

