---
title: "[자바(JAVA)] 객체(Object)와 인스턴스(Instance)"
categories:
- JAVA
tags: 
- [JAVA, Object, Instance]
date: 2021-08-10
last_modified_at: 2021-08-10
toc: true
toc_sticky: true
toc_label: "객체와 인스턴스"
---

# 객체(Object)

속성과 동작(=기능)(=필드와 메소드)를 가진 것
{: .notice--info}


## 객체 생성 방법

클래스로부터 객체를 생성하는 연산자 **new** 를 사용한다

```
클래스이름 변수명 = new 클래스이름();   
```

> Student.java

```java
public class Student{
}
```

> StudentObject.java

```java
public class StudentObject{
    Student s1 = new Student();
}
```

* Student.java 파일에 Student라는 클래스가 생성되었다. 그래서 이걸 사용하려고
* StudentObject.java 파일에서 s1이라는 이름으로 객체를 생성하였다!
* 이때 s1 객체는 **heap 메모리 영역**에 생성된다

* * *

# 인스턴스(Instance)

인스턴스란 클래스로부터 만들어진 객체
{: .notice--info}

* 클래스로부터 객체를 만드는 과정 = 인스턴스화

* * *

# 객체와 인스턴스의 구분

공부하다보면 객체와 인스턴스는 같은말로도 쓰이고 구분하여 쓰이기도하는 다른말이다🤔

* 객체 = 클래스의 타입으로 선언되었을 때 / 소프트웨어에 구현해야하는 대상      
* 인스턴스 = 메모리에 할당 되었을 때 / 소프트웨어에 구현된 실체   

> 내가 내린 구분은 아래와 같다

프로그램을 실행시켜서 메모리에 할당이 된 객체는 인스턴스이고,
내가 열심히 코딩하고 아직 구현중인 과정에서 클래스로부터 만들어진 것은 객체다.
{: .notice--info}

근데 여기저기 강의를 듣다보면 객체랑 인스턴스랑 혼용해서 이야기하기도 해서!!   
일단 둘은 비슷하게 쓰이는 단어지만, 명확하게는 같은것이 아니라는것을 인지하기로 했다.

