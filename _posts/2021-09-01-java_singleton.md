---
title: "[자바(JAVA)] 싱글톤 패턴(Singleton Pattern)"
categories:
- JAVA
tags: 
- [JAVA, Singleton, DesignPattern]
date: 2021-09-01
last_modified_at: 2021-09-01
toc: true
toc_sticky: true
toc_label: "싱글톤 패턴(Singleton Pattern)"
---

## 싱글톤 패턴

변수에 static 키워드가 있으면, 그 클래스의 인스턴스들이 공유하는 클래스 변수가 된다.
이 특성을 이용한 패턴이 싱글톤 패턴이다.
프로젝트 내부에서 단 한개만 존재해야 하는 인스턴스를 생성해야 할 경우에 사용한다.
전역변수를 사용하지 않고 객체를 하나만 생성하도록 하며, 생성된 객체를 어디에서든지 참조할 수 있도록 하는 디자인 패턴.

## 싱글톤 패턴 구현 방법

1. 생성자에 private을 접근제한자로 설정
2. static으로 객체를 구현
3. 객체의 getter 구현(외부에서 사용할 수 있도록)

-> 인스턴스의 유일성이 보장됨

>Company.java

```java
package singleton;

public class Company {
	
	//객체
	//변경되지 않을것이므로 private, 단 하나만 있을것이므로 static선언.
	private static Company instance = new Company();

	//생성자
	//내가 생성자 제공하지 않으면 default 생성자를 제공하므로, 직접 생성자를 선언해준다.
	//외부에서 Company 생성자를 선언하지 못하도록 private
	private Company() {} 

	// 외부에서 instance변수를 사용할 수 있도록 만든 메소드. 외부에서 사용해야하므로 public, return타입은 Company. 객체를 생성하지 않고 이 메서드를 불러올 수 있도록 static을 선언해준다.
	public static Company getInstance() {
		//방어적으로 만든 코드. private 로 생성된 생성자는 본인 class에서는 호출할수있어서 Company로 호출이 가능함. 
		if(instance == null) {
			instance = new Company();
		}
		return instance;
	}
	
}
```

> CompanyTest.java

```java
package singleton;

public class CompanyTest {

	public static void main(String[] args) {

		Company c1 = Company.getInstance(); //싱글톤 패턴으로 구현된 객체를 호출할때는 이렇게 호출한다.
		Company c2 = Company.getInstance();
		
		System.out.println(c1);
		System.out.println(c2); // 출력해보면 c1과 c2의 주소가 같은것을 확인할 수 있다.
	}

}
```


