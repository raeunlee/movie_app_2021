# Creating React JS
"[https://raeunlee.github.io/movie_app_2021](https://raeunlee.github.io/movie_app_2021)"
css 작업은 하지 않았음!

### 설치해야 할 것

- node
- npm
- npx
- git

### 리액트JS를 위해 알아야할것

- html, css
- javascript(basic 수준)

### 리액트를 이용한 웹사이트

- 에어비엔비
- 넷플릭스
- 스포티파이
- 슬랙

### 깃에 업로드

```bash
#레포지토리 생성후
$ git add .
$ git commit -m "내 레포지토리 주소"
$ git commit -m "커밋 메시지 작성"
$ git push origin master
```

### 깃헙 페이지 만들고 업로드

- 깃헙 페이지 설치

```bash
$ npm i gh-pages #깃헙 페이지 설치
```

- package.json 파일하단에 homapage 넣기!

무조건 소문자로 쓰기, 띄어쓰기 불가!

```json
"homepage" : "https://{내깃헙이름}.github.io/{내깃헙프로젝트이름}"
```

- package.json 파일 scripts에 deploy와 predeploy 명령어 만들기

```json
...,

"scripts" : {
	...
	...
	"deploy" : "gh-pages -d build",
	"predeploy" : "npm run build"
},

...
```

deploy는 build 폴더를 upload함 

build 폴더를 얻는 방법: npm run build를 실행!

npm run build를 실행하면 우리에게 build 폴더를 제공함

deploy를 먼저 호출하면 predeploy가 자동으로 실행됨!

```bash
# 파일 변경시에 build, deploy 다시해주기!
$ npm run build 
$ npm run deploy
```
