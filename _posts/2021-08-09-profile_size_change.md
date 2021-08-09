---
title:  "깃허브 블로그 프로필 사이즈 조절하기"
categories:
- Github_Blog
tags: 
- jekyll
date: 2021-08-09
last_modified_at: 2021-08-09
---


## 깃허브 블로그 프로필 사이즈 조절하는 방법

minimal-mistakes 기준
{: .notice}

_sass/minimal-mistakes/_sidebar.scss 에서

```
/*
   Author profile and links
   ========================================================================== */

.author__avatar {
  display: table-cell;
  vertical-align: top;
  width: 36px;
  height: 36px;

  @include breakpoint($large) {
    display: block;
    width: auto;
    height: auto;
  }

  img {
    max-width: 110px;
    border-radius: 50%;

    @include breakpoint($large) {
      padding: 5px;
      border: 1px solid $border-color;
    }
  }
}
```
img 부분을 수정한다.

나는 padding값이 싫어서 0px로 바꾸고, max-width 를 200px로 키우고, border-radius를 30%로 바꾸었다!