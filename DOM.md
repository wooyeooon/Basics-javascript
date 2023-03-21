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

console.log(Array.from(nodeList).reverse());
```

```javascript
// N.parentElement

// 노드의 부모 요소를 반환한다.

const el = document.querySelector(".child");
console.log(el.parentElement); // <div class"parent">..</div>
```

```javascript
// E,closest()

// 자신을 포함한 조상 요소 중 'CSS 선택자'와 일치하는,
// 가장 가까운 요소를 반환한다.
// 요소를 찾지 못하면, `null`값을 반환한다.

const el = document.querySelect(".child");

console.log(el.closest("div"));
console.log(el.closest("body"));
console.log(el.closest(".hello"));
```

```javascript
// N.previousSivling / N.nextSivling

// 노드의 이전 형제 혹은 다음 형제 노드를 반환한다.

const el = document.querySelect(".child");
console.log(el.previousSivling);
console.log(el.nextSivling);
```

```javascript
// E.previousElementSivling / E.nextElementSivling

// 요소의 이전 형제 혹은 다음 형제 요소를 반환 한다.

const el = document.querySelect(".child");
console.log(el.previousElementSivling);
console.log(el.nextElementSivling);
```

```javascript
// E.chidren
// 요소의 모든 자식 요소를 반환한다.
cosnt el = document.querySelect('.parent)
console.log(el.childeren)

console.log(Array.from(el.childeren))
```

```javascript
// E.firstElementchild / E.lastElementChild
// 요소의 첫 번째 자식 혹은 마지막 자식 요소를 반환한다.

const el = document.querySelect(".parent");

console.log(el.firstElementChild);
console.log(el.lastElementChild);
```
