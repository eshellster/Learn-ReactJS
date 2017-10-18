# ReactJS 배우기
[codecademy.com  Learn ReactJS](www.codecademy.com)
## 준비
- 컴퓨터에 Node 6 이상으로 설치. [nodejs](https://nodejs.org)

- create-react-app을 전역설치 한다. [Create React App](https://github.com/facebookincubator/create-react-app)
```shell
npm install -g create-react-app
```

- 설치할 위치로 이동하고 명령어를 입력한다. (간혹 postinstall 에러가 발생함으로 설치 명령에 `sudo`를 기입한다. )

```shell
sudo create-react-app my-app

cd my-app
npm start
```
----

## JSX 도입부

### JSX 기본 단위를 JSX 엘리먼트라 부른다.

JSX 엘리먼트는 정확히 HTML과 같아보인다.

```jsx
<h1>Hello world</h1>
```

----

### JSX 엘리먼트와 그것을 감싸는 것

JSX 엘리먼트는 자바스크립트 표현식으로 취급된다. 따라서 자바스크립트가 사용되는 곳이나 갈 수 있다.
다음은 변수 안에  담겨지는 JSX 엘리먼트의 예제이다.

```jsx
const navBar = <nav>I am a nav bar</nav>;
```
다음은 객체 안에 담겨지는 몇몇 JSX 엘리먼트의 예제이다.

```jsx
const myTeam = {
  center: <li>Benzo Walli</li>,
  powerForward: <li>Rasha Loa</li>,
  smallForward: <li>Tayshaun Dasmoto</li>,
  shootingGuard: <li>Colmar Cumberbatch</li>,
  pointGuard: <li>Femi Billon</li>
};
```
----

### JSX 안의 속성(Attributes)

JSX 엘리먼트는 HTML 엘리먼트와 같이 속성을 가지고 따옴표""로 감싼다.
```jsx
my-attribute-name = "my-attribute-value"
```

 JSX 엘리먼트 안의 속성 예제

```jsx
<a href="http://www.example.com">Welcome to the Web</a>;

const title = <h1 id="title">Introduction to React.js: Part I</h1>;
```

하나의 JSX 엘리먼트는 HTML관 같이 여러 속성을 가질 수 있다.

```jsx
const panda = <img src="images/panda.jpg" alt="panda" width="500px" height="500px" />;
```

**중요한 규칙** 쌍으로 쓰이지 않는 태그의 경우 HTML의 형식과 다르게 위의 `<img />` 와 같이 마지막에 `/` 를 넣느다.



#### 연습문제 JSX 엘리먼트 코드

- [ ] 상수 `p1`을 선언, =  jsx  `<p></p>` 엘리먼트 작성, `<p></p>`사이에 "foo" 쓰기

- [ ] 상수 `p2`을 선언, =  jsx  `<p></p>` 엘리먼트 작성, `<p></p>`사이에 "foo" 쓰기

- [ ] `p1`의  엘리먼트 `<p></p>` 에  attribute `"large"` 기입

- [ ] `p2`의  엘리먼트 `<p></p>` 에  attribute `"small"` 기입


```jsx
const p1 = <p id="large">foo</p>
const p2 = <p id="small">bar</p>
```

----

### 중첩된 JSX

둘 이상의 행을 사용할 경우 괄호 안에 JSX표현식을 래핑해야 합니다.

 이제 *중첩 된* JSX 표현식은 변수로 저장되거나 함수에 전달 될 수 있습니다. 

```jsx
const theExample = (
   <a href="https://www.example.com">
     <h1>
       Click me!
     </h1>
   </a>
 );
```

### 중요한 규칙 하나 더 `<div></div>` 로 최종 감싸기

정상 작동 코드

```jsx
const paragraphs = (
  <div id="i-am-the-outermost-element">
    <p>I am a paragraph.</p>
    <p>I, too, am a paragraph.</p>
  </div>
);
```

 `<div></div>` 로 감싸지 않아 작동하지 않는 코드

```jsx
const paragraphs = (
  <p>I am a paragraph.</p> 
  <p>I, too, am a paragraph.</p>
);
```

----

###  JSX 랜더링

화면에 랜더링 하기 위한 JSX 표현식

```jsx
import React from 'react';
import ReactDOM from 'react-dom';

ReactDOM.render(<h1>Hello world</h1>, document.getElementById('app'));
```

javaScript는 대소문자를 구분함으로 ReactDOM 문구를 작성시 주의한다.

----

### 실전 ReactDOM 랜더링 

**create-react-app** 설치 후 생긴 폴더와 파일들을 아래와 같이 일치 시키다.

```
my-app

    |— node_modules

    |— public

    |		|— index.html

    |— src

    |		|— index.js

     package-lock.json

     package.json
```

**index.js**

```jsx
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
ReactDOM.render(<div><h1>Render me!</h1></div>, document.getElementById('app'));
```

**index.html** 을 아래의 코드로 바꾼다.

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8">
        <title>Learn ReactJS</title>
    </head>
    <body>
    	<main id="app"></main>
	</body>
</html>
```
**index.css** 를 **index.js**과 같은 위치인 **src** 폴더에 생성하고 아래 코드를 삽입한다. **건너뛰어도 무방하다.**

```css
div {
position: relative;
height: 100%;
width: 100%;
padding-top: 10px;
}

h1, h2 {
margin-left: 5%;
margin-right: 5%;
}
```

----

### 웹에서 확인하기

프로젝트 폴더로 이동해 `npm start`  입력한다.

```shell
npm start
```

아래와 같이 출력되면 정상이다.

```shell
Compiled successfully!

You can now view learn-react-js in the browser.

  Local:            http://localhost:3000/

  On Your Network:  http://192.168.0.23:3000/

Note that the development build is not optimized.

To create a production build, use npm run build.
```

 출력된 정보의 URL을 주소창에 입력해 확인한다. 축하!

----

index.js의 `document.getElementById('app')` 가  index.html의 `<main id="app"></main>` 로 전달된다. 

or

 index.html의 `<main id="app"></main>` 가 index.js의 `document.getElementById('app')` 를 호출한다.

----

### ReactDOM.render()로 변수 전달

변수 `toDoList`를 선언하고 JSX엘리먼트들을 담아 `ReactDOM.render()`에서 첫번째 인수(프로그램 내의 변수)로 호출한다.

```jsx
const toDoList = (
  <ol>
    <li>Learn React</li>
    <li>Become a Developer</li>
  </ol>
);

ReactDOM.render(
  toDoList, 
  document.getElementById('app')
);
```

