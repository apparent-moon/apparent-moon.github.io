---
title: "[Blog] 깃허브 블로그 포스트 날짜 표기하기"
categories:
- Github_Blog
tags: 
- jekyll
date: 2021-08-09
last_modified_at: 2021-08-09
---


## 깃허브 블로그 포스트 날짜 표기하는방법

minimal-mistakes 기준
{: .notice}



포스트 밑에 보면 "최대 1분 소요" 로 뜨는게 거슬렸다...!

![img](/image/positing_date_showing_how_to.png)

(로컬에서 테스트했을때 작성했던 게시글ㅎㅎ;;)


_config.yml 파일 맨 밑쪽에 보면 이렇게 코드가 작성되어있다.

```
# Defaults
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: ture
      comments: # true
      share: true
      related: true
```

여기서 read_time: true를 false로 바꾸고,
show_date: true로 변경시킨다.

> 변경 후

(path: "_pages" 이쪽 세션은 여기저기 찾아보다가 추가한 부분이다.
404 페이지가 떠도 프로필이 보이게 하기위해서 사용한다고 해서 추가했다!)

```
# Defaults
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: false
      comments: # true
      share: true
      related: true
      show_date: true

  - scope:
      path: "_pages"
      type: pages
    values:
      layout: single
      author_profile: true
```

변경하고나면 

![img](/image/positing_date_showing_how_to_result.PNG)

"최대 1분 소요" 이런게 안뜨고 날짜만 나오게 된다 😉
