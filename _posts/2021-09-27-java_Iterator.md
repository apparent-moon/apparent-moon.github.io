---
title: "[자바(JAVA)] Iterator"
categories:
- JAVA
tags: 
- [JAVA, Iterator]
date: 2021-09-27
last_modified_at: 2021-09-27
toc: true
toc_sticky: true
toc_label: "Iterator"
---

## Iterator
컬렉션 프레임워크(Collection Framework)에서 요소를 순회할 때 사용한다.

get 메소드가 제공되지 않는 경우에 활용하여 객체를 순회할 때 유용하다👍

```java
Iterator<타입> Iterator변수명 = 순회할 컬렉션의 변수명.iterator();

[ex] : list 라는 arrayList가 선언되어있고 String 타입의 요소들이 들어가있을 때
Iterator<String> iterator = list.iterator();
```

iterator를 선언하면 컬렉션의 맨 처음을 가르키는 상태가 된다.

### Iterator와 함께 자주 사용되는 메소드

#### hasNext()

이후에 요소가 있는지 확인하여 t/f를 반환한다.

#### next()

다음에 있는 객체를 반환해준다.

