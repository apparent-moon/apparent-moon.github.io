---
title: "[SpringBoot(스프링부트)] DTO와 VO"
categories:
- SpringBoot
tags: 
- [SpringBoot, DTO, VO]
date: 2021-10-05
last_modified_at: 2021-10-05
toc: true
toc_sticky: true
toc_label: "DTO와 VO"
---

## DTO(Data Transfer Object)

- 계층간에 데이터를 주고받을 때 사용하지만, 일회성으로 사용된다.
- 데이터베이스의 데이터를 매핑하기 위한 데이터 객체다.
- 데이터베이스로부터 데이터를 얻어 Service나 Controller 등으로 보낼 때 사용한다.
- getter/setter만 가지고있다.

```java
public class UserDTO {
    private String name;
    private Integer age;
    private String phoneNumber;
    private String address;

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public Integer getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String getPhoneNumber() {
        return phoneNumber;
    }

    public void setPhoneNumber(String phoneNumber) {
        this.phoneNumber = phoneNumber;
    }

    public String getAddress() {
        return address;
    }

    public void setAddress(String address) {
        this.address = address;
    }
}
```

## VO(Value Object)

- VO는 `객체` 의 의미를 가진다.
- 안에 있는 내용물이 값 자체를 의미해서 read only 특징을 가진다.
- equals, hashcode를 재정의해줘야한다.


-> VO는 추후 공부하게되면 한번 더 살펴보기. DTO와 VO에 관해서 구분하는 글들이 많아서 일단 정리해뒀다.