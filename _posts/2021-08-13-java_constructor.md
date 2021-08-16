---
title: "[자바(JAVA)] 생성자(Constructor)"
categories:
- JAVA
tags: 
- [JAVA, Constructor]
date: 2021-08-13
last_modified_at: 2021-08-13
toc: true
toc_sticky: true
toc_label: "생성자"
---

## 생성자(Constructor)

이름이 클래스명과 동일하고 리턴 자료형이 없는 메소드(=함수)   
new 연산자와 클래스로부터 객체를 생성할때 호출된다.   
(class 내부에 만들어두고, 나중에 객체를 생성하기위해서 생성자를 호출할 때 new 연산자랑 같이 쓰인다는 말임)

### 생성자를 사용하는 이유

인스턴스를 만들고, 인스턴스의 속성을 `초기화`하기 위해서 사용한다.

+ 인스턴스의 속성을 초기화 한다는 말이 이해가 조금 어려워서 추가 설명!

>Student.java

```java
public class Student{
    int studentGrade = 1;
    String studentName;
    int studentNumber;

    Student(String studentName, int studentNumber){
        this.studentName = studentName;
        this.studentNumber = studentNumber;
    }
}
```

>StudentTest.java
```java
public class StudentTest{
    public static void main(String[] args){
        Student studentKim = new Student("김댕댕", 20210001);
        Student studentLim = new Student("임댕댕", 20210002);
    }
}
```

(this에 대한 설명은 아래쪽에!)

학생 클래스에서 필드에서 studentGrade는 1학년으로 초기화했고,   
studentName과 studentNumber는 아무것도 선언해주지 않아 null과 0이 들어가있을 것이다.

인스턴스의 값을 초기화 해주는 방법은 아래와 같다.(=필드에 다른 값을 지정하는 방법은 아래와 같다)
1. 필드에서 초기화해준다. (=클래스에서 생성할 때 값을 지정해준다.)
2. 생성자에서 초기화해준다.

StudentKim, studentLim과 같은 객체 생성 시점에 값을 주어야 다양한 객체가 생성될 수 있다.   
처음 필드에 선언 할 때 부터, studentName을 지정해주면 모두가 그 이름을 사용하게 되니까...!   
그래서 인스턴스 초기화를 할 때 생성자를 사용한다.

### 생성자를 정의하는 방법

1. 클래스와 이름이 동일해야 한다
2. 반환타입이 없어야 한다.

### 기본생성자(default constructor)

모든 클래스에는 생성자가 반드시 존재한다.   
만약 클래스 내부에 생성자 선언을 하지 않으면 컴파일러가 자동으로 기본 생성자(=디폴트 생성자)를 생성해준다!

#### 기본생성자(default constructor) 형태

```java
1. 클래스가 public으로 만들어진 경우
public 클래스명(){

}

2. 클래스에 접근제한자(public)가 없는 경우
클래스명(){

}
```

### 명시적으로 생성자 선언하는 방법 (=사용자가 직접 생성자 선언하기)

```java
클래스(매개변수1, 매개변수2...){

//초기화 코드를 입력!

}
```

명시적으로 생성자를 선언 한 경우, 기본 생성자 호출이 불가능하다!

### 생성자 오버로딩

생성자는 다양한 방법으로 객체가 생성될 수 있도록 오버로딩을 지원한다!

즉, 매개변수를 다르게 해서 생성자를 여러 개 사용할 수 있다는 의미!

> Student.java

```java
public class Student{
    
    int studentNumber;
    int studentGrade;
    String studentName;

    Student(){
    }

    Student(int studentNumber, String studentName){
        this.studentNumber = studentNumber;
        this.studentName = studentName;
    }
}
```

매개변수가 없는 `Student()`도 선언이 가능하고, 매개변수가 있는 `Student(int studentNumber, String studentName)` 생성자도 선언했다. 멤버변수가 모두 매개변수로 포함된 `Student(int studentNumber, int studentGrade, String studentName)` 도 만들 수 있다!   
이렇게 생성자를 여러개 만드는 행위가 생성자오버로딩!


### this

위에 예제들을 보면 `this.studentNumber` 와 같이 this를 사용했다.   

this는 객체 자신을 말한다.

`this.studentNumber = studentNumber`에서

왼쪽의 `studentNumber`는 멤버변수인 `studentNumber`를 가리키고`(int studentNumber)`   
오른쪽의 `studentNumber`는 매개변수인 `studentNumer`를 가리킨다.`(Student(int studentNumber))`

변수이름을 다르게 해서 사용도 가능하지만, this를 사용하면 다른사람이 나중에 내 코드를 봤을 때 파악하기도 쉽기때문에 통상적으로 this를 사용해서 생성자를 생성한다.

* * *
생성자에 대한 정의가 제대로 잘 잡히지 않으면 나중에 헷갈리고 혼란스러워서 정리하다보니 글이 길어졌다.   
앞으로 생성자는 제발 안 까먹고싶다...!!!!!!!!!!