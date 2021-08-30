---
title: "[자바(JAVA)] 자바 메소드 정리"
categories:
- JAVA
tags: 
- [JAVA, Algorithm, Method]
date: 2021-08-30
last_modified_at: 2021-08-30
toc: true
toc_sticky: true
toc_label: "클래스 별 메소드"
---

자바문제를 풀면서 사용한 메소드들을 정리해두기 위해서 만든 포스팅입니다.
* * *

## Scanner 클래스
next()
- 문자열을 하나 읽음(String형태로 읽음)

charAt(N)
- 읽은 문자열을 인덱스로 접근하여 N번 째 문자만 받아올 때 사용. 
```java
Scanner sc = new Scanner(System.in);
char c = sc.next().charAt(0) //콘솔로 받아온 문자열의 첫번째 문자를 c라는 변수에 저장한다.
```

## Character 클래스
toUpperCase()
- 대문자로 바꿔준다

toLowerCase()
- 소문자로 바꿔준다

```java
char c = 'a';
c = Character.toUpperCase(c);
System.out.println(c); //A
```

isLowerCase()
- 소문자여부를 확인해서 false/true값을 return한다.

isUpperCase()
- 대문자여부를 확인해서 false/true값을 return한다.

```java
char c = 'a';
boolean result = Character.isLowerCase(c);
System.out.println(result); //true
```

## String 클래스
toCharArray()
- 문자열을 배열형태로 바꿈

toUpperCase()
- 대문자로 바꾼다

```java
String s= "abcdE";
System.out.println(s.toUpperCase()); //ABCDE
```
