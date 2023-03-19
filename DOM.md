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
