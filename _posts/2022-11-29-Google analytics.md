---
layout: post
title: "Google analytics 추가"
date: 2022-11-29 1:34:30 +0900
categories: jekyll update
comments: true
---

# Google analytics 추가

1. google analytics 홈페이지에 접속후 애널리틱스 계정을 만든다.

2. "관리"에서 새로운 Google 애널리틱스 속성을 만든다.

3. "관리"에서 새로운 데이터 스트림을 추가한다. 웹을 클릭하고 스트림을 추가하기 위한 설정을 완료한다.

4. 관리 -> 관리자 -> 속성 -> 데이터 스트림에서 측정ID를 복사

5. _config.yml 파일에 아래 코드 추가
```html
analytics:
provider               : "google-gtag" 
google:
    tracking_id          : "G-MN3R6WW2Q3"
includes/head.html
```
6. includes 폴더에 analytics 파일을 생성하고 아래 코드 추가
<!-- Google tag (gtag.js) -->
    <script async src="https://www.googletagmanager.com/gtag/js?id=복사한 측정ID"></script>
    <script>
    window.dataLayer = window.dataLayer || [];
    function gtag(){dataLayer.push(arguments);}
    gtag('js', new Date());

    gtag('config', '');
    </script>