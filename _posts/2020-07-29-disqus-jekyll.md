---
title:  "jekyll에 댓글기능 추가하기 ft. Disqus"
tags: [disqus, jekyll, 댓글]
use_math: true
comments: true
---

## Disqus란? 

다른 블로그 사이트들을 보면 기본적으로 댓글 기능이 포함이 되어 있는데

jekyll에는 댓글 기능이 없기 때문에 따로 댓글 서비스 기능을 추가해줘야 하는데

그 댓글 서비스 이용하게 되는데 그게 바로 [Disqus](https://disqus.com/){:target="_blank"} 입니다

## 설치

### 회원가입
[https://disqus.com/profile/signup/](https://disqus.com/){:target="_blank"} 에 접속을 하여 회원가입을 합니다 

![disqus 회원가입](/assets/images/20200729/disqus_signup.png)

### 사이트 설정

![disqus 설정1](/assets/images/20200729/disqus_setting_01.png)

I want to install Disqus on my site 선택

![disqus 설정2](/assets/images/20200729/disqus_setting_02.png)

Website Name을 입력하고 Category를 선택하고 Create site 선택

![disqus 설정3](/assets/images/20200729/disqus_setting_03.png)

Select a plan에서 Basic 플랜을 Subscribe now 선택

![disqus 설정4](/assets/images/20200729/disqus_setting_04.png)

Jekyll 선택

![disqus 설정5](/assets/images/20200729/disqus_setting_05.png)

jekyll에 disqus에 코드삽입 방법을 알려주는 페이지 입니다

jekyll에서 post를 생성할때 

    
    ---
    layout: post
    title:  "jekyll에 댓글기능 추가하기 ft. Disqus"
    permalink: /:categories/:year/:month/:day/:title/
    date:   2020-07-29 14:30:00 +0900
    categories: posts
    tags: [disqus, jekyll, 댓글]
    comments: true
    ---

comments: true 이 코드를 추가하고

Universal Embed Code 를 클릭을 합니다

![disqus 설정6](/assets/images/20200729/disqus_setting_06.png)

_layouts/default.html

```liquid
{% if page.comments %}
    Universal Embed Code 삽입
{% endif %}
```
    
    
post 레이아웃 부분에 해당 코드를 삽입합니다

