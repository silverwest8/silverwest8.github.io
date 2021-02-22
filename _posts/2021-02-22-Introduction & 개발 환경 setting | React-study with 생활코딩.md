---
title: "Introduction & 개발 환경 setting | React-study with 생활코딩"
permalink: /develop/
layout: posts
subtitle: "React-study with 생활코딩"
date: 2021-02-22 18:22
tag: [Github io, React, 생활코딩, 개발환경]
---

# React-study with 생활코딩

## Introduction & 개발 환경 setting

페이스북에서 만든 자바스크립트 UI 라이브러리

```jsx
<Top><Top/> <Sidebar><Sidebar/>
```

와 같은 사용자 정의 태그를 "컴포넌트"라고 함

1. 가독성
2. 재사용성
3. 유지보수

coding → run → deploy

공식문서

[Getting Started - React](https://reactjs.org/docs/getting-started.html)

## #coding

node.js 설치 후

tool chain :: create-react-app

```bash
$ npx create-react-app .
$ create-react-app -v
$ npm run start
```

npm이란?

npx → 얘를 임시로 설치해서 한번만 사용(최신버전의 reacte)

## #run

### 샘플 웹앱 파악

- **public**

index.html 내 root id가 있음

- **src**

엔트리파일인 index.js에서 App컴포넌트를 렌더링

App.js —> class type or function type 

css와 App 내용 지우고 깨끗하게 시작!

크롬→ 개발자도구 켜고 캐시 지우고 새로고침

1.7MB? 개발편의성을 위해 파일의 무게가 무겁고 보안문제가 많음.

## #deploy

production 모드로 빌드할때는 

```bash
$ npm run build
$ npm install -g serve
or
$ npx serve -s build
```

build 폴더가 만들어지고 공백같은 불필요 정보를 없앰 → 125KB밖에 안됨

pure.html

시멘틱 태그 <header> <nav> <article>

내용이 많아지면 분리해서 코드를 짜고싶을 때 리액트로 컴포넌트를 만들면 잘 정리정돈 됨

리액트는 최종적으로 웹브라우저에 html을 공급(react 자체 공급이 아님)

App.js 의 코드

```jsx
class App extends Component {
  render() {
    return (
      <div className="App">
        <Subject></Subject>
      </div>
    )
  }
}
```

는 자바스크립트가 아님(유사 자바스크립트)

태그를 그대로 쓸 수 있도록 만든 jsx 임 → 이것을 자바스크립트 코드로 컨버팅 해주는 것