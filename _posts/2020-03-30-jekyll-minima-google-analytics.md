---
layout: post
title:  "jekyll minima 테마 블로그에 구글 애널리틱스 적용방법"
permalink: /:categories/:year/:month/:day/:title/
date:   2020-03-30 17:00:00 +0900
categories: posts
comments: true
---

## 구글 추적ID 받기
구글 애널리틱스에 가입 [https://analytics.google.com/](https://analytics.google.com/){:target="_blank"}

사이트 등록 후 추적ID를 받습니다

![구글 애널리틱스 추적ID](/assets/google-analytics-trackid.png)

## jekyll _config.yml에 입력

<code>_cofing.yml</code> 파일에 google_analytics: 추적ID 입력

    google_analytics: 추적ID

로컬 환경에선 작동을 안하기 때문에 운영환경(github-page)에서 확인

[https://github.com/jekyll/minima#enabling-google-analytics](https://github.com/jekyll/minima#enabling-google-analytics){:target="_blank"}