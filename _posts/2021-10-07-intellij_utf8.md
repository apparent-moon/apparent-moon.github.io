---
title: "[IntelliJ] 인텔리제이 UTF-8 설정하기"
categories:
- IntelliJ
tags: 
- [IntelliJ, UTF-8]
date: 2021-10-07
last_modified_at: 2021-10-07
toc: true
toc_sticky: true
toc_label: "IntelliJ UTF-8 설정하기"
---

## 윈도우 운영체제에서 한글을 사용할 경우 필요한 설정이다.

## 파일 - 설정 - 파일 인코딩

전역 인코딩, 프로젝트 인코딩, 프로퍼티파일에 대한 디폴트 인코딩 -> 모두 UTF8로 변경해준다.

체크박스는 안해도 상관없는것 같은데 나는 그냥 해줬다!

![img](/image/intellij_utf8.PNG)

## 도움말 - 사용자지정VM옵션지정편집

```
-Dfile.encoding=UTF-8
```

위 코드를 추가한다.

![img](/image/intellij_utf8_2.PNG)

## build.Gradle에 추가하기

```
compileJava.options.encoding = 'UTF-8'

tasks.withType(JavaCompile) {
    options.encoding = 'UTF-8'
}
```

위 코드를 추가한다.

![img](/image/intellij_utf8_3.PNG)

* * * 

대체로 두번째 방법까지로도 해결되는것같은데, 나는 세번째방법까지 추가해야 동작했다.