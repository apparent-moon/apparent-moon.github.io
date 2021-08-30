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

객체는 생성자를 호출하고나서 생성된다.   
자식 클래스에서 객체를 생성할때는 부모클래스에서 생성자를 호출한 후 자식클래스에서 생성자를 호출하여 객체가 생성되는 방식이다. 자식 클래스에서 객체를 생성할 때, 우리 눈에는 자식클래스에서만 생성자를 통해 객체를 생성하는것으로 보이지만, 사실은 이와 같은 과정을 통해서 생성이 되는 것이다.

부모클래스에서 생성자 호출 -> 자식클래스에서 생성자 호출 -> 자식클래스에서 객체 생성  

이 때, 자식클래스에서는 부모 클래스의 생성자를 호출하기 위해서 super()를 사용한다.

부모 클래스에 기본 생성자가 없다면 super()를 반드시 명시해줘야 하고, 있다면 명시하지 않아도 컴파일러에서 생성해준다.

>Animal.java

```java
public class Animal{
    public String name;
    public String type;

    public Animal(String name, String type){
        this.name = name;
        this.type = type; // type 은 땅,하늘,물... 이런거라고 가정!
    }
}
```

>Lion.java

```java
public class Lion extends Animal{
    public int legs;

    public Lion(String name, String type, int legs){
        super(name, type);
        this.legs = legs;
    }
}
```

Lion이 자식 클래스이고, Animal이 부모 클래스일때 부모클래스에 기본생성자가 없으므로 자식클래스에서 명시적으로 super()를 사용하여 생성자를 호출했다.

