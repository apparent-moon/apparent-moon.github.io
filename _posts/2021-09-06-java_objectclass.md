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

## Object 클래스

Object 클래스는 모든 클래스의 최상위 클래스로, `java.lang` 패키지에 포함되어 있다!   
그래서, 모든 클래스는 Object 클래스를 상속 받아서 사용한다.   
컴파일러가 `extends Object` 를 추가해줘서 따로 정의해서 사용하지 않아도 된다.

```java
//우리가 이렇게 작성해도
class Student{

}

//컴파일러가 이렇게 넣어준다
class Student extends Object{

}
```

## Object 클래스의 메소드들

하위 클래스에서는 상위 클래스의 메소드를 재정의해서 사용할수 있으므로, 우리는 Object 클래스에 포함되어있는 **일부 메소드를 재정의**해서 사용할수있다.
(Object 클래스 내부에서 final로 선언된 메소드는 제외하고 선언이 가능함.)

![img](/image/java_objectclass.PNG)

이클립스에서 확인한 재정의 가능한 메소드들!

- clone()
- equals()
- hashCode()
- toString()
- finalize() -> deprecated되었음

Object 클래스의 다른 메소드들은 [Object class](https://docs.oracle.com/javase/7/docs/api/java/lang/Object.html)에서 확인!   



### clone()

객체의 원본을 복제할 때 사용하는 사용한다.(동일한 인스턴스를 생성한다.)   
OOP프로그램에서 정보은닉, 객체 보호의 관점에서는 좋지 않은 사용법.   
`implements Cloneable`을 클래스에 명시해서 사용해야한다.

### equals()

두 인스턴스의 주소 값을 비교하여 T/F를 반환해준다.

```java
//st1객체, std2객체가 있을 때
Student std1 = new Student("김철수");
Student std2 = new Student("김철수");
Student std3 = new Studnet("박운수");


System.out.println(std1.equals(std2)); //true 객체의 타입이 같고 id(여기서는 김철수)값이 같으므로 true다.
System.out.println(std1.equals(std3)); //false
```

### hashCode()

인스턴스의 저장 주소를 반환해준다.   
(hash는 정보를 저장, 검색하는 자료구조를 의미한다.)

+++

실제로 저장되어있는 가상 메모리 주소는 아래와 같이 검색할 수 있다.
```java
System.out.println(System.identityHashCode(객체명));
```

### toString()

객체의 정보를 String으로 바꾸어서 사용할 때 사용된다.
매개값(타입)이 기본타입일 경우에는 `System.out.print` 를 이용하여 해당 값을 그대로 출력할 수 있지만, 매개값이 객체일 경우에는 toString()메소드를 사용해서 리턴값을 받아 호출해야한다.

