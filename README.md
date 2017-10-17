# ReactJS 배우기
[codecademy.com  Learn ReactJS](www.codecademy.com)
## 준비
- 컴퓨터에 Node 6 이상으로 설치. [nodejs](https://nodejs.org)

- create-react-app을 전역설치 한다. [Create React App](https://github.com/facebookincubator/create-react-app)
```shell
npm install -g create-react-app
```

- 설치할 위치로 이동하고 명령어를 입력한다. (간혹 postinstall 에러가 발생함으로 설치 명령에 "sudo"를 기입한다. )

```shell
sudo create-react-app my-app

cd my-app
npm start

```

## [서론] JSX 도입부

### JSX 기본 단위를 JSX 엘리먼트라 부른다.

```jsx
<h1>Hello world</h1>
```

JSX 엘리먼트는 정확히 HTML과 같아보인다.

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
### JSX 안의 속성(Attributes)
JSX 엘리먼트는 HTML 엘리먼트와 같이 속성을 가지고 따옴표""로 감싼다.
```jsx
my-attribute-name = "my-attribute-value"
```
