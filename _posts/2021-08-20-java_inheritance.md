---
title: "[자바(JAVA)] 상속(inheritance)"
categories:
- JAVA
tags: 
- [JAVA, Inheritance]
date: 2021-08-20
last_modified_at: 2021-08-20
toc: true
toc_sticky: true
toc_label: "상속(inheritance)"
---

## 상속(inheritance)

기존의 클래스를 재사용하여 새로운 클래스를 만들 떄 사용하는 방식이다.

기존의 클래스를 `부모클래스(parent class), 상위클래스`   
기존의 클래스를 재사용하여 만드는 _새로운 클래스_ 를 `자식클래스(child class), 하위클래스` 로 부른다.

상위클래스는 하위 클래스보다 더 **일반적인 개념과 기능**을 가지고   
하위클래스는 상위클래스보다 더 **구체적인 개념과 기능**을 가진다.

### 클래스 상속

하위클래스 작성법은 아래와 같다.
```java
class 자식클래스명 extends 부모클래스명{

}
```

`extends` 키워드를 사용하면 된다.

만약 Flowers 클래스가 상위클래스이고 하위클래스로 Roses를 생성하고싶다면

```java
class Roses extends Flowers {

}
```

Roses class 를 이렇게 작성하면 된다.

### 자바 상속의 특징

1. 여러 개의 부모 클래스 상속이 불가하다.

아래와 같이 작성이 불가하고, 부모클래스는 1개만 가능하다.

```java
class 자식클래스명 extends 부모클래스명1, 부모클래스명2 ... {
//이렇게 작성이 불가능함!
}
```

2. private 으로 접근제한자가 설정된 필드는 자식클래스로 상속이 불가능하다.

이부분은 접근제한자를 공부하면서 공부했지!

private를 **protected**로 작성하면 자식클래스에서 상속이 가능하다.

그리고 자식클래스와 부모클래스가 서로 다른 패키지에 존재한다면 default 접근제한자여도 상속이 불가능하다.

- public -> 다른패키지여도 상속O   
- default -> 같은 패키지에서 상속O   
- protected -> 같은 패키지에서 상속O   
- private -> 상속 X

### super()

**이쪽은 좀 더 이해하고 올릴 예정. 포스팅 추후 수정 예정** 
