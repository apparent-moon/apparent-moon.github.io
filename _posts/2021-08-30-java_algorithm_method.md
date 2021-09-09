---
title: "[자바(JAVA)] 자바 메소드 정리"
categories:
- JAVA
tags: 
- [JAVA, Algorithm, Method]
date: 2021-08-30
last_modified_at: 2021-09-09
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

getNumericValue()
- char형을 int 형으로 바꾸어서 return해준다.

## String 클래스
toCharArray()
- 문자열을 배열형태로 바꿈

toUpperCase()
- 대문자로 바꾼다

```java
String s= "abcdE";
System.out.println(s.toUpperCase()); //ABCDE
```

split()
- 문자열 배열 형식으로 리턴.

split( , limit)
- limit 의 개수만큼 문자열을 나눈다

```java
        String str = "Hi Today is rainy";
        String[] result = str.split(" "); //공백을 기준으로 문자열을 나눈다
        String[] result2 = str.split(" ", 2);
        System.out.println(Arrays.toString(result));//배열 형식으로 리턴하므로, Arrays 클래스의 toString메소드를 이용해서 출력했다.
        //[Hi, Today, is, rainy] limit이 없을때는 공백을 기준으로 자른다.
        System.out.println(Arrays.toString(result2)); //[Hi, Today is rainy] limit을 2로 주어서 문자열을 2개로 나누었다.
```

## Array 클래스
sort()
- 배열을 오름차순으로 정렬해준다.
```java
        int[] arr = {99, 10, 35, 1, 55};
        Arrays.sort(arr);
        for(int i = 0; i < arr.length; i++){
            System.out.print(arr[i] + " "); // 1 10 35 55 99 
        }
```

## Integer 클래스
equals()
= 두 값을 비교한다.
```java
public class Main {
    public static void main(String[] args) {
        Integer intA = Integer.valueOf(10);
        Integer intB = Integer.valueOf(15);
        

        if( intA.equals(intB) ){
            System.out.println("True");
        }else{
            System.out.println("False");
        }//결과 : False

        //이런식으로도 가능하다!
        if( intA.intValue() == intB.intValue() ){
            System.out.println("True");
        }else{
            System.out.println("False");
        }//결과 : False
    }
}
```