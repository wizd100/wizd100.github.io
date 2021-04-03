---
title:  "jekyll에 댓글기능 추가하기 ft. Disqus"
tags: [disqus, jekyll, 댓글]
use_math: true
comments: true
published: false
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

Configure 버튼 선택

![disqus 설정6](/assets/images/20200729/disqus_setting_06.png)

Complete Setup 버튼 선택해서 완료

![disqus 설정7](/assets/images/20200729/disqus_setting_07.png)

Setting 선택

![disqus 설정8](/assets/images/20200729/disqus_setting_08.png)

shortname 값을 복사합니다

Minimal Mistakes 테마의 경우 disqus 설정을 <code>_config.yml</code>에서 설정합니다

~~~
comments:
  provider               : "disqus" # false (default), "disqus", "discourse", "facebook", "staticman", "staticman_v2", "utterances", "custom"
  disqus:
    shortname            : shortname입력 # https://help.disqus.com/customer/portal/articles/466208-what-s-a-shortname-
~~~

post 헤더 부분에

~~~
---
title:  "jekyll에 댓글기능 추가하기 ft. Disqus"
tags: [disqus, jekyll, 댓글]
use_math: true
comments: true
---
~~~

comments: true  추가 후 완료

git push 후 사이트에서 확인

![disqus 설정9](/assets/images/20200729/disqus_setting_09.png)

