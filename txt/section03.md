# Section3 : 리액트 기초 및 실습 컴포넌트

## 24.모듈 소개
- React를 구성하는 모든 기본 기능들 및 핵심적인 기능들(JSX 구문)
- component 구축 방법
- Data 사용법

## 25. 컴포넌트란 무엇인가? 왜 리액트는 컴포넌트의 전부라고 하는가?
- 즉 비용 추적기같은 것을 구축할 때 리액트같은 것을 사용한다면 작업은 훨씬 더 수월할 것입니다
- 아주 사소한 것들에 신경쓸 필요도 없고 오류도 덜 발생할 것입니다.

### Components를 쓰는 이유?
- 모든 사용자 인터페이스들은 결국 컴포넌트로 구성되기 때문입니다

### Components란?
- 재사용 가능(반복하지 않도록 한다.)
- 우려사항들을 분리할 수 있다.(작고 관리 가능한 단위로 유지할 수 있게 해준다.)
- 여러분이 구축하는 것이 어떤 것이든 함수를 사용해서 작업하는 경향이 있고 코드를 여러 개의 작은 함수로 나누고 호출이 가능함.

## 26. 리액트 코드는 "선언적 방식"으로 작성되었습니다

### Component가 어떻게 만들어지는가?
- HTML
- CSS
- JavaScript
위 세가지가 결합을 해서 제작을 하는 것이다.

### React 와 Component
- 리액트로 재사용 가능하며 반응하는 컴포넌트를 만들수 있다.(HTML, CSS, JavaScript)
- 이런 컴포넌트를 만들기 위해서는 선언적 접근 방식을 사용한다.
- 리액트로 작업할 때는 항상 원하는 최종 상태, 즉 목표 상태 또는 다양한 상황에 따라
  다른 목표 상태를 정의하는 것이 아주 중요합니다.
- 최종 상태와 어떤 상황에서 어떤 상태가 사용되어야 하는지 정의하면 됩니다
- 자신만의 HTML 요소들을 만들고 결합해서 사용자 인터페이스를 구축할 수 있습니다

## 27. 새 React 프로젝트와 NodeJS에 대한 참고 사항
```
강의에서 NodeJS(새 React 프로젝트를 생성하는데 필요한 도구)를 설치합니다.
NodeJS를 다운로드하고 설치하는 방법과 더불어 React 프로젝트를 생성하는 방법을 배울 예정입니다.
새로 생성한 React 프로젝트를 실행하는 도중에 ‘digital envelope routines unsupported’ 오류가 발생한다면, 그 이유는 NodeJS 버전 때문입니다.
이 오류가 발생한다면, package.json 파일에서 다음을 교체하십시오.

"start": "react-scripts start"
부분을 아래와 같이 바꿔주세요.
"start": "react-scripts --openssl-legacy-provider start

그리고

"build": "react-scripts build"
부분을 아래와 같이 바꿔주세요.
"build": "react-scripts --openssl-legacy-provider build"
```

## 28. 새로운 React 프로젝트와 Node.js에 관한 공지사항
새로운 React 프로젝트 & Node.js에 관한 공지

다음 강의에서는 React 프로젝트를 생성할 때 사용하는 도구인 Node.js를 설치해야 합니다.

React 프로젝트 생성 방법과 Node.js 다운로드 및 설치 방법을 알려드릴 텐데요, Node.js 17 버전은 다운받으시면 안 됩니다! 현재 해당 버전에서는 생성한 프로젝트가 작동하지 않거든요.

대신 Node.js의 LTS 버전을 다운로드해주세요. 다음 링크에서 해당 버전(LTS)을 다운로드할 수 있습니다. [Node.js 다운로드](https://nodejs.org/en/download/)

## 29. 새로운 React 프로젝트 생성하기
- [React 프로젝트 생성](create-react-app.dev)
- 일부 기본적인 리액트 코드 파일이 있는 미리 설정된 폴더들과 상용화할 수 있는 리액트 앱을
구축할 수 있도록 돕는 가장 중요한 환경설정 파일들이 있습니다

### 크리에이트 리액트 앱으로 생성된 프로젝트
- 웹 개발 서버는 여러분의 로컬 컴퓨터에서 그 응용프로그램을 미리보기 할 수 있다.
- 코드나 기타 다른 것들이 변경될 때마다 브라우저가 자동적으로 페이지를 업데이트하는 방식으로
이 응용프로그램을 미리 볼 수 있습니다.
- 리액트 코드를 좀 더 정리를 할 수가 있다.

React.JS 프로젝트 생성 명령어

```
// react 프로젝트 생성
npx create-react-app react-complete-guide
// CD (change directory) 폴더 이동 명령어
cd react-complete-guide
// 개발 서버 오픈
npm start
```

src라는 폴더에서 App.js가 저희가 보여지는 
