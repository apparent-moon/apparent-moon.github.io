---
title: "[자바(JAVA)] 배열(Array)"
categories:
- JAVA
tags: 
- [JAVA, Array]
date: 2021-08-27
last_modified_at: 2021-08-27
toc: true
toc_sticky: true
toc_label: "배열(Array)"
---

## 배열이란

같은 타입의 데이터가 연속된 공간에 나열된 형태를 말한다.   
각 데이터에 인덱스를 부여해놓은 자료구조다.   
한번 생성된 배열의 길이는 수정이 불가능하다.

### 인덱스란?

배열에서 인덱스란, 배열 요소의 일련번호를 말한다.

## 배열 선언 방법

```java
1. 자료형[] 변수명;

ex) int[] array;

2. 자료형 변수[];

ex) int array[];
```

### 배열은 메모리의 어디에 생성될까?
배열은 참조변수로 **힙(heap)** 영역에 생성된다.

## 배열 객체 생성 방법

```java
//값이 있을 때
1. 자료형[] 변수명 = {값, 값, 값, 값 ... };

ex) int[] array = {1, 2, 3, 4, 5};

//값이 나중에 결정 되지만, 배열을 미리 만들때
1. 자료형[] 변수명 = new 자료형[길이지정];
2. 자료형 변수명[] = new 자료형[길이지정];

//int값만 저장이 되고 길이가5이고 배열이름이 array인 배열을 생성.
ex) int[] array = new int[5];
    int array[] = new int[5];
```

## 향상된 for문

사실 이 array 포스팅의 목적은 이것 작성이 목표다 ㅎㅅㅎ   

```java
for( 배열에 담긴 변수가 저장되는곳 : 배열)
```

> main.java

```java
public class main {
    public static void main(String[] args){
        int array[] = {1, 2, 3, 4, 5}; //int형으로 배열을 선언

        for( int x : array){ 
            System.out.println(x);
        }
    }
}
```
1. int형으로 1,2,3,4,5가 들어가있는 array라는 이름의 배열을 선언해줌
2. `for(int x : array)`에서 array는 내가 for문을 돌리고 싶은 배열을 오른쪽에 써준다.
3. `for(int x : array)`에서 int x는 오른쪽에 써있는 배열안에 있는 값의 자료형과 변수명을 써주었다. 변수명은 내가 임의로 지어준것으로 뭐든 들어갈 수 있다.!
4. array의 length만큼, 즉 array에 들어있는 배열의 항목 수 만큼 for문을 돌면서 배열의 항목을 print해준다.

출력 결과   
![img](/image/java_array.PNG)

