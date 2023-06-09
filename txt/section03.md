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

## 31. 표준 리액트 프로젝트 분석하기

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

src라는 폴더에서 index.js이 페이지가 로드하면 가장 먼저 실행하는 파일

```
// 개발 서버 오픈
npm start
전달하기 전에 코드를 변형해서 추가 기능이 브라우저에서 작동하도록 해줌
```

```
ReactDOM이라는 객체를
react-dom이라는 서드 파티 라이브러리에서 가져온다는 뜻으로
이 라이브러리는 의존성 중 하나의 로컬에 다운로드 및 설치 됨

package.json 파일을 보면 두 개의 React의존성이 있다.
react, react-dom에 의존을 한다.

react-dom이라는 패키지에서 React DOM 객체를 내보내고 이을 index.js로 가져왔습니다.
```

## public 폴더의 index.html

- 이 단일 HTML 파일이 브라우저에서 로딩되는데, 오직 이 HTML 파일만이 React 애플리케이션에서 사용될 겁니다.

## createRoot 메서드 역할

```
해당 메서드는 React에게 이것이 React 애플리케이션의 루트(root)이자
React 애플리케이션이 렌더링될 주된 위치라는 점을 알려 줍니다
```

파일 이름은 항상 .js를 빼고 입력을 해야됨
그 이유는 import를 할 때, 확장자가 없어야 합니다.

## 32. JSX 소개

- 자바스크립트 XML를 의미한다.
- JSX로 입력을 하면 자동으로 브라우저에서 작동하는 코드로 변환됨.
- 개발자로서 작성하기 쉽다
- 기본적인 자바스크립트를 알아야 하는 것은 있습니다.

## 33. 리액트 작동 방식

- 궁극적으로 화면에 나타는 것은 HTML코드입니다.
- 최종상태를 정의하기만 하면 리액트는 이런 것들을 화면에 불러오기 위한 지시사항들을 뒷단에 생성할 것입니다

## 34. 첫 번째 사용자 지정 컴포넌트 만들기

- 컴포넌트 트리
- 폴더명 지을 때, 대문자로 시작하는 한 단어이고
- 한 단어 안에 여러 단어를 결합하면 중간에 시작하는 서브 단어는 대문자로 시작해야 합니다
- import로 불러오고 태그를 쓸 때, <태그명 />를 추천한다.

## 35. 더 복잡한 JSX 코드 작성

- 여러가지 태그를 한 번에 묶어주는 div 태그가 필수이다.

## 36. 기본 CSS 스타일 추가

- JSX에서는 className으로 클래스를 작성을 할 수 있다.

## 37. JSX에서 동적 데이터 출력 및 표현식 작업하기

- 동적 데이어 출력

```
const 변수명 = 변수값;
<div>{변수명}</div> // 변수값이 나온다.
```

## 38. "props"를 통해 데이터 전달하기

- props는 properties를 나타내는 것
- 사용자 지정 컴포넌트의 속성을 설정할 수 있습니다
- 컴포넌트 재사용이 가능하다
- 다른 컴포넌트에게 데어터 전달이 가능하다

## 39. 컴포넌트에 "일반" JavaScript 논리 추가하기 컴포넌트를 여러 컴포넌트로 분할하기

- 변수명으로 따로 빼서 함수값에다 넣고 그 값을 props로 이용을 한다.

## 40. 컴포넌트를 여러 컴포넌트로 분할하기

- 파일 이름 정할 떄, 첫 문자는 대문자로 정하기

## 41. 연습하기: 리액트 및 컴포넌트 기본 사항(문제), 42. 연습하기: 리액트 및 컴포넌트 기본 사항(정답)

## 43. "컴포지션(composition,합성)"의 개념("children prop")

- 의미 : 컴포넌트 간의 합성
- 목적 : 컴포넌트 안에 컴포넌트를 전달하고 싶은 경우
- 장점 : 코드의 재사용성을 향상 / JSX 요소를 좀 더 유연하고 밀접하게 다룰 수 있습니다

## 44. 첫번째 요약

- React의 핵심 구문 & JSX
- Component을 이용한 작업
- 데이터 공유(props로 작업을 함)
- 웹은 JSX를 인식을 못하고 HTML만 인식을 한다.

## 45. JSX 자세히 보기

- JSX코드는 단지 읽기 쉽고 편한 문법에 불과했기 때문이다
- 브라우저는 JSX코드를 지원하지 않는다
- 두 가지 종속요소(react, react-dom)가 있다

- JSX 구문을 사용하지 않는 경우

```
import React from 'react';

// return React.createElement('생성하는요소', '요소를 설정하는 객체', '컨텐츠')

return React.createElement(
    'div',
    {},
    React.createElement('h2', {}, "Let's get started!"),
    React.createElement(Expense, { items: expenses })
  );

```

## 46. 컴포넌트 파일 구성하기-

- 실질적으로 보여지는 부분을 UI폴더를 생성 후 옮긴다
- 공통이 되는 파일은 키워드로 폴더를 만든 후 그 안에 넣는다

## 47. 대체 함수 문법(syntax)

```
함수문법
function App () {}

화살표 함수
const App = () => {}

변경이 가능하다
```

## 퀴즈1

### 1

- 질문 : React.js에서는 어떤 유형의 코드로 작성하나요?
- 답 : 선언형(Declarative) JavaScript 코드

### 2

- 질문 : “JSX”란 무엇일까요?
- 답 : React 프로젝트에서만 활성화하는 특수한 비표준 구문이다.

### 3

- 질문 : 왜 “컴포넌트”를 React의 모든 것이라고 할까요?
- 답 : 모든 UI는 결국 어러 빌딩 블록(='컴포넌트')으로 구성되며, 따라서 사용자 인터페이스를 "컴포넌트의 조합"이라고 생각할 수 있다.

### 4

- 질문 : “선언형”은 무슨 뜻인가요?
- 답 : 원하는 결과(대상 UI등)을 정의하고 라이브러리(React)가 단계를 구성한다.

### 5

- 질문 : “React 컴포넌트”란 무엇일까요?
- 답 : 일반적으로 표시되어야 하는 HTML(JSX) 코드를 반환하는 JavaScript함수이다.

### 6

- 질문 : React 앱은 커스텀 React 컴포넌트를 몇 개 가져야 하나요?
- 답 : 사용자 마음대로

### 7

- 질문 : 올바른 문장은?
- 답 : React를 사용해서 DOM 노드에서 마운트되는 하나의 루트 컴포넌트를 가진 컴포넌트 트리를 구축합니다.

### 8

- 질문 : "컴포넌트 트리"란 무엇을 뜻하나요?
- 답 : 루트 노드 아래에 여러 컴포넌트가 중첩되어 있는 것을 뜻한다

### 9

- 질문 : 어떻게 컴포넌트 간에 데이터를 전달하나요?
- 답 : "프로퍼티"라고 잘 알려진 "커스텀 HTML 속성"을 통해

### 10

- 질문 : React 컴포넌트 내부의 동적 데이터(반환된 JSX 코드)는 어떻게 출력하나요?
- 답 : 아무 JS 표현식을 단일 중괄호({}, 여닫음)로 감싸 사용한다.
