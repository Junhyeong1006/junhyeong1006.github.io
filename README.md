# https://junhyeong1006.github.io/

# 프로젝트 빌드 과정

## 1. YAT 테마 적용

아래 사진에서 fork를 선택하여 username.github.io라는 이름의 repository를 생성  
  
![image](https://user-images.githubusercontent.com/105621923/204254810-b15e6701-b3a1-4239-b1f6-690137269b56.png)

그 후에 ```git clone```을 통해 로컬 저장소에 받아온다.
#
## 2. Jekyll 설치

jekyll 공식 사이트: 
https://jekyllrb-ko.github.io/

Windows용 Ruby + Devkit
https://rubyinstaller.org/downloads/

Ruby를 설치  

```gem install jekyll bundler```를 통해
Jekyll과 Bundler를 설치한다.  

```jekyll -v```을 통해 Jekyll이 올바르게 설치되었는지 확인한다.

#
## 3. Jekyll 사이트 생성

```jekyll new . --force```을 통해
블로그를 만드는 로컬 디렉토리에 Jekyll을 설치 

```bundle exec jekyll serve``` 을 실행 후,
localhost:4000 접속하여 블로그와 테마가 잘 작동하는지 확인한다.

잘 작동하는 지를 확인 한 후 ```git add *```를 통해 stage를 하고  
```git commit -m "message"```으로 commit을 한다.  
그리고 git push를 통해 업로드를 한다.  

잠시후 만들어진 github 블로그 주소에 들어가서 로컬과 같이 잘 작동하는지를 확인 한다.
#
## 4. 댓글 기능 추가
Disqus 사이트에 들어간다.

Disqus 가입 & 세팅 (platform : jekyll 선택)
_config.yml 에 아래 코드를 추가해 파일 수정
```
comment:
  provider: "disqus"
  disqus:
    shortname: "junhyeong"
```
disqus 홈페이지에서 Universal Code를 _layouts/post.html 에 적용 (PAGE_URL과 PAGE_IDENTIFIER은 나의 정보에 맞게 수정)

내가 만든 각 post파일들에 아래의 코드 추가
comments: true

## 5. favicon 추가

favicon으로 추가할 이미지를 준비한다.  

favicon generator 사이트에 들어가 이미지를 favicon으로 바꾼다.

Download the generated favicon을 클릭해서 파일을 다운받는다.

assets 폴더에 다운로드 받은 파일을 복사하여 넣는다.

_includes에 새로운 파일의 head.html에 
```html
<link rel="icon" type="image/png" href="/assets/favicon.ico">
```
위 코드를 작성한다.

#
## 6. Google analytics 구현 
[알고싶으면 드러와](https://junhyeong1006.github.io/jekyll/update/2022/11/28/Google-analytics.html)

#
## 7. topic post 생성
[내용이 궁금하면 드러와](https://junhyeong1006.github.io/jekyll/update/2022/11/25/special-lecture.html)