---
title: "[자바(JAVA)] 클래스(Class)"
categories:
- JAVA
tags: 
- [JAVA, Class]
date: 2021-08-10
last_modified_at: 2021-08-10
toc: true
toc_sticky: true
toc_label: "클래스"
---

# 클래스(Class)

객체에 대한 속성과 기능이 구현되어있는 설계도 
{: .notice--info}

비유하자면

* 쿠키틀 -> 클래스   
* 쿠키틀로 만든 쿠키 -> 인스턴스

## 클래스 생성 규칙

하나의 java 파일에는 하나의 클래스를 두는것이 원칙이지만,   
여러개의 클래스를 생성할 경우, public은 단 하나만 만들 수 있고 public class는 자바 파일의 이름과 동일해야 한다

> Student.java

```java
public class Student {
	int studentID;
	String studentName;
	int grade;
	String address;
 }
```

* public(접근 제어자)

* class(클래스를 만드는예약어)

* Student(사용자가 정의하는 클래스의 이름)

* studentID, sudentName, grade, address (property or attribute 라고 부름. 클래스의 속성이다.)

Student라는 클래스 안에 studentID 변수, studentName변수, grade 변수, address 변수가 있는것!

