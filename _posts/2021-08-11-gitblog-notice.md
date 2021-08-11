---
title: "[Blog] 깃허브 블로그 notice 추가하기(다른 색의 박스 추가하기)"
categories:
- Github_Blog
tags: 
- jekyll
date: 2021-08-11
last_modified_at: 2021-08-11
toc: true
toc_sticky: true
toc_label: "notice 추가하기"
---

## 깃허브 블로그 notice 추가하기

minimal-mistakes / jekyll 사용자 기준
{: .notice}

* * *

notice가 뭐냐면 바로 

제가 notice 입니다
{: .notice--warning}

이건 Kramdown이라는 Markdown의 개조판에서 사용하는 문법인데, Kramdown이 지킬의 기본 렌더러라서 지킬에서 사용이 가능하다고 하는것 같다.

글을 작성하다보면 박스 형태의 무언가가 가끔 필요한데

```
이건 코드 작성용 박스니까 다른 박스가 필요했다.
```

그래서 notice를 발견하고 유용하게 사용하고있다.

>지킬을 이용하지않고 다른 방법으로 깃허브 블로그를 운영할경우, Kramdown 문법을 지원하는지 확인해보아야 한다!

### notice 사용 방법

```
제가 notice 입니다
{: .notice--warning}
```

쓰고자 하는 말을 쓰고 밑에줄에 `{: .notice}` 를 작성하면 된다!

나는 노란색? 주황색? 박스를 쓰고 싶어서 notice뒤에 --warning을 붙였다.

### notice 종류

``` 
default Notice
{: .notice}
  
primary Notice
{: .notice--primary}
 
info Notice
{: .notice--info}
 
warning Notice
{: .notice--warning}
 
danger Notice
{: .notice--danger}

success Notice
{: .notice--success}
```

default Notice
{: .notice}
  
primary Notice
{: .notice--primary}
 
info Notice
{: .notice--info}
 
warning Notice
{: .notice--warning}
 
danger Notice
{: .notice--danger}

success Notice
{: .notice--success}

종류가 많지만... 맘에 드는색의 박스를 골라서 쓰면 될것같다 😎

* * *
참고   

jekyll kramdown: [jekyll-kramdown][jekyll-link]

[jekyll-link]: https://jekyllrb.com/docs/configuration/markdown/#kramdown   

minimal-mistakes: [minimal-mistakes][minimal-link]

[minimal-link]: https://mmistakes.github.io/minimal-mistakes/docs/utility-classes/#notices