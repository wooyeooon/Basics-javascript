#### DOM (Document Object Model)

```javascript
// DOM이란 HTML 문서를 객체로 표현한 것으로,
// JS에서 HTML을 제어할 수 있게 해준다.

const element = document.querySelector("h1");
console.log(elementtextContent); // Hello world!
```

```javascript
// Node vs Element

// - 노드(Node): HTML 요소, 텍스트, 주성 등 모든 것을 의미
// - 요소(Element): HTML 요소를 의미

const parent = document.querySelector(".parent");

// 부모 요소의 모든 자식 노드 확인!
console.log(parent.childNodes);

// 부모 요소의 모든 자식 요소 확인!
console.log(parent.children);

class N {}
class E extends N {}

console.dir(E); // class E
console.dir(N); // class N
console.dir(E.__proto_); // class N

console.dir(Element); // Element ()
console.dir(Node); // Node ()
console.dir(Element.__proto_); // Node ()
```

```javascript
// document.getElementById()

// HTML `id` 속성(Attributes) 값으로 검색한 요소를 변환한다.
// 여러 요소가 검색되면, 가장 먼저 찾은 요소만 변환된다.
// 검색 결과가 없으면, `null`을 반환한다.

const el = document.getElementById("child2");
console.log(el); // child2의 Id을 가지고 있는 html 요소를 가져온다.
```

```javascript
// document.querySelector()

// 'CSS 선택자'로 검색한 요소를 하나 반환한다.
// 여러 요소가 검색되면, 가장 먼저 찾은 요소만 변환된다.
// 검색 결과가 없으면, `null`을 반환한다.

const el = document.querySelector(".child:first-child");
console.log(el); // <div class="child">1</div>
```

```javascript
// document.querySelectorAll()

// 'CSS 선택자'로 검색한 모든 요소를 `NodeList`로 반환한다.
// `NodeList` 객체는 `.forEach()`를 사용할 수 있다.

const nodeList = document.querySeletorAll(".child");
console.log(nodeList);
nodeList.forEach((el) => console.log(el.textContent));
```
