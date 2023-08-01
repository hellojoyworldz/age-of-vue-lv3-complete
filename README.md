# 해커 뉴스 공식 사이트 만들기

- CLI 3.x  
  [해커 뉴스 공식 사이트 주소](https://news.ycombinator.com/)  
  [해커 뉴스 API 문서 주소](https://github.com/tastejs/hacker-news-pwas/blob/master/docs/api.md)

## 애플리케이션 라우터 설계

news, ask, jobs

- 페이지 이동이 가능한 뷰 라우터
- 컴포넌트 공통화

## CLI 2.x vs CLI 3.x

[Vue CLI 사이트](https://cli.vuejs.org/)  
[Vue CLI webpack](https://cli.vuejs.org/guide/webpack.html#working-with-webpack)  
[webpack-simple 템플릿 깃헙 주소](https://github.com/vuejs-templates/webpack-simple)

- 명령어

  - 2.x: vue init webpack-simple(프로젝트 템플릿 이름) 파일위치
  - 3.x: vue create 프로젝트이름

- 웹펙 설정 파일

  - 2.x: 노출 O
  - 3.x: 노출 X

- 프로젝트 구성

  - 2.x: 깃헙의 템플릿 다운로드
  - 3.x: 플러그인 기반으로 기능 추가

- ES6 이해도

  - 2.x: 필요 X
  - 3.x: 필요 O

## ESLint

자바스크립트에서 도움말 역할을 해줌. 문법 검사기

```javascript
// case 1
var a = 10;

// case 2
// 가독성을 위해 세미콜론(;)을 생략하기도 한다.
// 자바스크립트 해석기(실제 실행할 때)가 코드를 분석하면서 ; 넣어준다
var a = 10

// ESLint는 ; 찍게끔 유도함
// 어느 구간에서 자바스크립트 해석기가 ; 를 붙여야할지...
// 즉, 오류가 날 수 있다.
if(a===10) console.log('10이다') b() c()

// 트레일링 콤마 (trailing comma)
// 한 쌍이 오는 경우에는 콤마(,) 생략하는데
// eslint에서는 , 를 강조 - 한 쌍이 오더라도 , 붙임
components: {
  '컴포넌트 이름': 컴포넌트 내용,
}
```

### ESLint 설정 끄는 방법

1. 라인 추가

```javascript
<template>
  ...
</template>
<script>
  // component 마다 script에 라인 추가
  /* eslint-disalbe */
</script>
```

2. vue.config.js
   https://cli.vuejs.org/config/#lintonsave  
   vue-cli 프로젝터의 루트 디렉토리(package.json 파일이 있는 위치)에서 vue.config.js 파일 생성

```javascript
// vue.config.js
module.exports = {
  lintOnSave: false,
};
```

## router

https://router.vuejs.org/installation.html  
`npm i vue-router@3.5.3 --save`

dependencies :  
앱을 실행시키는데 필요한 동작을 담당하는 라이브러리  
배포할 때 포함되어야할 라이브러리

```javascript
// package.json
"dependencies": {
  "core-js": "^3.8.3",
  "vue": "^3.2.13",
  "vue-router": "^3.5.3"
}
```

## 참고 사이트

[Node.js 공식 사이트 주소](https://nodejs.org/ko)  
[VSCode 공식 사이트 주소](https://code.visualstudio.com/)  
[Vue.js 스타일 가이드 주소](https://v2.vuejs.org/v2/style-guide/?redirect=true)
