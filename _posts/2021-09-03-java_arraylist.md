---
title: "[자바(JAVA)] ArrayList"
categories:
- JAVA
tags: 
- [JAVA, ArrayList, CollectionFramework]
date: 2021-09-03
last_modified_at: 2021-09-03
toc: true
toc_sticky: true
toc_label: "ArrayList"
---

## ArrayList란

컬렉션 프레임워크(Collection Framework)의 `List 인터페이스`에 포함되어있는 구현클래스다.

- 객체를 인덱스로 관리한다.
- 저장 용량이 부족하면 자동으로 증가한다.
- 객체를 저장할 때 자동으로 인덱스가 증가한다.

## ArrayList 선언 방법

```java
ArrayList<타입> 변수명 = new ArrayList<타입>();

//이렇게 사용해도 된다.
ArrayList<타입> 변수명 = new ArrayList<>();
```

## ArrayList 사용 방법

> ArrayList 객체 추가

```
ArrayList변수명.add(값);
변수명,add(인덱스번호,값);
```

> ArrayList의 크기

```
ArrayList변수명.size();
```

> ArrayList 객체 삭제

```
ArrayList변수명.remove(인덱스번호);
ArrayList변수명.clear(); //모든 값이 제거된다
```

> ArrayList 객체 얻기

```
ArrayList변수명.get(인덱스번호);
```

### 같은 클래스 안에서 사용 예시

```java
import java.util.*;

public class ArrayListtest {

	public static void main(String[] args) {
		
		ArrayList<String> student = new ArrayList<>();
		
		//값 저장
		student.add("김철수");//String 객체를 저장한다.
		student.add("이진수");
		student.add("박현수");
		student.add("최민수");

		//크기 구하기
		int size = student.size();
		System.out.println(size); //4
		System.out.println("==========");

		//인덱스의 객체 얻기
		String getStudent = student.get(1);
		System.out.println(getStudent); //이진수
		System.out.println("==========");
		
		//인덱스 삭제하기
		student.remove(1); //1번객체가 삭제된다. student ArrayList 상태 : 김철수 박현수 최민수
		student.remove(1); //1번객체가 삭제된다. student ArrayList 상태 : 김철수 최민수
		for(i = 0; i<student.size(); i++
			String stu = student.get(i);
			System.out.print(stu); // 김철수최민수
		}
	}
}
```

* * *

### 타입에 객체 넣어서 사용 예시

주로 ArrayList를 사용할때 타입에 객체를 넣어서 사용한다. 그럴때는 new 로 객체를 생성해서 add한다.

> Student.java

```java
public class Student {

	private int grade;
	private String name;

	public Student() {}
	
	public Student(int grade, String name) {
		this.grade = grade;
		this.name = name;
	}
	
	public int getGrade() {
		return grade;
	}

	public void setGrade(int grade) {
		this.grade = grade;
	}

	public String getName() {
		return name;
	}

	public void setName(String name) {
		this.name = name;
	}

	public void showStudentInfo() {
		System.out.println(grade + "," +name);
	}
}
```

> StudentTest.java

```java
import java.util.*;

public class StudentTest {

	public static void main(String[] args) {
		
		ArrayList<Student> student = new ArrayList<Student>();
		
		student.add(new Student(1, "김철수"));
		student.add(new Student(2, "이진수"));
		student.add(new Student(3, "최민수"));
		
		for(int i =0; i<student.size(); i++) {
			student.get(i).showStudentInfo();
		}
	}
}
```
