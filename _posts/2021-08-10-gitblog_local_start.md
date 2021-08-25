---
title: "[Blog] 깃허브 블로그 로컬에서 구동하기"
categories:
- Github_Blog
tags: 
- jekyll
date: 2021-08-10
last_modified_at: 2021-08-10
---


## 깃허브 블로그 로컬에서 구동하는 방법

맨날 까먹어서 내 깃블로그에 기록해두기로 한다.
다른 방법들도 많겠지만 나는 항상 이렇게 접속한다.

1. ruby prompt 를 구동한다.
![img](/image/local_1.PNG)
2. 내 PC에 github.io 를 clone 했던곳으로 이동한다.
```
cd 주소입력
```
![img](/image/local_2.PNG)
3. chcp 65001 를 입력한다. (인코딩을 부여하는 명령어다. 오류가 나지않도록)
```
chcp 65001
```
![img](/image/local_3.PNG)
4. 밑에 코드를 입력하여 지킬 서버를 구동한다. (이걸 맨날 까먹어서==;;)
```
bundle exec jekyll serve
```
![img](/image/local_4.PNG)
내 블로그의 경우 conflict가 뜨는에 일단 문제는 없어서 그냥 사용중... 언젠가 고쳐야지!
5. 
```
http://127.0.0.1:4000/
``` 
들어가면 로컬에서 지킬 블로그 구동 완료!
![img](/image/local_5.PNG)

