---
title: "[자바(JAVA)] 오버라이딩과 오버로딩"
categories:
- JAVA
tags: 
- [JAVA, Overriding, Overloading]
date: 2021-10-27
last_modified_at: 2021-10-27
toc: true
toc_sticky: true
toc_label: "오버라이딩과 오버로딩"
---

## 오버라이딩(Overriding)

부모 클래스로부터 상속받은 메소드를 자식 클래스에서 재정의 하는 것

```java

public class Overriding{
    class Person{
        void walk(){
            System.out.println("걷습니다");
        }
    }

    class Child extends Person{
        @Override
        public void walk(){
            System.out.println("아장아장 걷습니다.")
        }
    }
}
```


## 오버로딩(Overloading)

한 클래스내에 메소드의 이름이 같지만 매개변수가 다른 메소드를 정의하는 것

```java
public class Overloading{
    class void hello(){
        System.out.println("안녕");
    }

    class void hello(String name){
        Sysetm.out.println(name+"안녕");
    }
}
```