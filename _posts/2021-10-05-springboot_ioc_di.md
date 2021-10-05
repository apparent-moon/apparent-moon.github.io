---
title: "[SpringBoot(스프링부트)] IoC와 DI"
categories:
- SpringBoot
tags: 
- [SpringBoot, IoC, DI]
date: 2021-10-05
last_modified_at: 2021-10-05
toc: true
toc_sticky: true
toc_label: "IoC, DI"
---

## IoC (Inversion of Control)

Java 객체를 new로 생성한것이 아닌 스프링 컨테이너를 통해서 객체를 관리 -> 객체 관리의 권한이 개발자가 작성하는 코드로부터 스프링이 담당하도록 넘어가서 `제어의 역전`이라고 한다.

## DI (Dependency Injection)

코드상에서 new를 통해 직접적으로 객체를 생성하지 않고 객체의 밖에서 객체를 넣어주는 방식을 말한다.
