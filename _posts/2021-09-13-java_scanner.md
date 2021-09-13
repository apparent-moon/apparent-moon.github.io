---
title: "[자바(JAVA)] 스캐너(Scanner)"
categories:
- JAVA
tags: 
- [JAVA, Scanner]
date: 2021-09-13
last_modified_at: 2021-09-13
toc: true
toc_sticky: true
toc_label: "스캐너(Scanner)"
---

## 스캐너(Scanner) 클래스

문제를 풀면서 자주 사용했는데, String값을 입력받을 때 `nextLine`을 써야할지 `next`를 써야할지 등등 헷갈리는 경우가 많아서 정리해두고자 한다.

스캐너는 `java.util` 패키지에서 제공하는 클래스다.

### 사용 방법

```java
Scanner scanner = new Scanner(System.in); // Scanner 타입의 변수 scanner 를 선언하고, 시스템의 입력장치로부터 읽는 Scanner를 생성한다.
String input = scanner.nextLint(); //String타입으로 입력받을거라 nextLine을 사용했다.
```

### System.in

콘솔에서 키보드의 데이터를 입력받을 수 있도록 하는 System 클래스의 in 정적 필드.

in -> 키보드 입력을 가리킨다.

## 스캐너(Scanner) 종류

대소문자를 꼭 맞춰서 써줘야한다

```
nextint -> X   
nextInt -> O
```

### String 타입
- next()   
띄어쓰기를 문자열의 끝으로 인식한다.

- nextLine()   
띄어쓰기를 문자열에 포함시켜주고, 엔터를 쳐야 문자열의 끝으로 인식한다.

### Int 타입
- nextInt()

### byte 타입
- nextByte()

### short 타입
- nextShort()

### long 타입
- nextLong()

### float 타입
- nextFloat()

### double 타입
- nextDouble()

### boolean 타입
- nextBoolean()

### BigDecimal타입
- nextBigDecimal()

### BigInteger타입
- nextBigInteger()

### char타입
char타입은 따로 입력받는 방법이 없다.
그래서 String타입으로 입력받은 후 char타입으로 변환해주어야한다.

#### charAt()

charAt은 string을 char타입으로 변환해주는 메소드다.

(괄호)안에는 출력할 문자열의 index번호를 입력하면 된다.

즉 `String`이라는 단어에서 `S` 를 출력하고싶다면 `charAt(0)`을 입력해주면 된다.

```java
Scanner sc = new Scanner(System.in);

char c = sc.next().charAt(0);
sc.close();

System.out.println(c);
```

## Scanner의 끝에는 sc.close();

현재는 단순하게 콘솔을 통해 입력받는 예시들을 많이 들었고 그런부분만 공부했는데, 나중에는 파일등을 통해 입력을 받는 경우도 있다고 한다. 그럴경우엔 꼭 사용해주어야 에러가 나지 않는다.   
지금과같이 키보드로 입력을 받는경우에는 별 상관 없다고 하지만, 습관을 미리 들여주는게 좋다고 생각한다.

```java
Scanner sc = new Scanner(System.in);

String str = sc.next();
sc.close();
```
