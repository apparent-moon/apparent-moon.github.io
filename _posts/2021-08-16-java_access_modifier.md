---
title: "[자바(JAVA)] 접근 제한자(Access Modifier)"
categories:
- JAVA
tags: 
- [JAVA, AccessModifier]
date: 2021-08-16
last_modified_at: 2021-08-16
toc: true
toc_sticky: true
toc_label: "접근제한자"
---

## 접근제한자

접근제한자는 객체 생성을 막거나, 외부 클래스에서의 사용을 제한하기 위해서 사용한다.

접근제한자에는 3가지 종류가 있다

0. default(밑에 3가지 접근제한자를 사용하지 않을 시 사용된다)
1. public
2. protected
3. private

접근 제한은

public > protected > default > private 

private 으로 갈수록 강화된다.

### default 접근 제한자


```java
class 클래스명{

}
```

같은 패키지에서는 제한없이 사용이 가능하지만 다른 패키지에서는 사용이 제한된다.

### public 접근 제한자

```java
public class 클래스명{

}
```

같은패키지뿐만 아니라 다른 패키지에서도 사용이 가능하다.

라이브러리 개발시에는 public 접근 제한자를 이용하여 만들자!

### protected 접근 제한자

```java
protected class 클래스명{

}
```
자식 클래스에서는 접근이 가능하지만, 다른 외부 클래스는 접근이 불가능하다.
만약 다른 패키지에 속한 클래스가 해당 클래스의 자식 클래스라면 호출이 가능함! => 자식 클래스면 다른 패키지라도 사용이 가능하다.

### private 접근 제한자

```java
private class 클래스명{

}
```

모든 외부 클래스에서의 접근이 불가능하다.