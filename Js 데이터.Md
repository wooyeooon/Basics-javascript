### Array (배열)

```javascript
const fruits = new Array("Apple", "Banana", "Cherry"); // new를 호출하면 생성자 함수, 자바스크립트 클래스라 부른다.
const fruits2 = ["Apple", "Banana", "Cherry"]; // 대열 리터럴 방식

console.log(fruits);
console.log(fruits2[1]); // 특정 데이터를 조회 하는 것을 인덱싱, 대광로 표기법 이라 한다.
console.log(fruits2.length); // 배열의 길이를 조회
```

### Object(객체)

```javascript
const user = new Object();
user.name = "Ukato";
user.age = 95;

console.log(user);

function User2() {
  this.name2 = "Ukato";
  this.age2 = 95;
}
const user2 = new User2();

console.log(user2);

const user3 = {
  name: "Ukato",
  age: 95,
};
const key = "name";

console.log(user3.age); // 점 표기볍 (객체 데이터 안에서 계속 사용이 가능하다.)
console.log(user3[key]); // 대괄호 표기법

const userA = {
  name: "Kato",
  age: 20,
};
const userB = {
  name: "ssss",
  age: 23,
  parent: userA,
};
console.log(userB);

fuction(함수);

function hello() {
  console.log("Hello!");
}

console.log(hello);

const getNumber = function () {
  return 123;
};
console.log(typeof getNumber());

const a = function () {
  console.log("A");
};

const b = function (c) {
  console.log(c);
  c();
};

b(a);
```

### 형 변환(Type Conversion)

```javascript
const a = 1; // Number
const b = "1"; // String

console.log(a === b); // === 일치 연산자 == 동등 연산자

// 참과 거짓 (Truthy & Falsy)

// 1) false
// 2) 0
// 3) null
// 4) undefined
// 5) NaN
// 6) ''
// 7) 0n

if (true) {
  console.log("참!"); // true
}
if (123) {
  console.log("참!"); // true
}
if ("0") {
  console.log("참!"); // true
}
if (0) {
  console.log("참!"); // false
}

const fruits = ["Apple", "Banana"];

if (fruits) {
  console.log("아이템이 들어있습니다.");
} // true
```

### 데이터 타입 확인

```javascript
const a = 123;

console.log(typeof a); // number

console.log(typeof "Hello"); //string
console.log(typeof "Hello" === "string"); //true
console.log(typeof "123" === "number"); //true
console.log(typeof "false" === "boolean"); //true
console.log(typeof "undefined" === "undefined"); //true
console.log(typeof "null" === "object"); //true
console.log(typeof [] === "object"); //true
console.log(typeof {} === "object"); //object
console.log(typeof function () {} === "function"); //function

// console.log(null.constructor) // Error 속성을 읽을 수 없기 때문에
console.log([].constructor === Array); // Array() {native code}, true
console.log({}.constructor === Object); // Object() { native code}, true

function checkType(data) {
  return Object.prototype.toString.call(data).slice(8, 01);
}
console.log(checkType("Hello")); // String
console.log(checkType(123)); // Number
console.log(checkType(false)); // Boolean
console.log(checkType(undefined)); // Undefined
console.log(checkType(null)); // null
console.log(checkType([])); // Array
console.log(checkType({})); // Object
console.log(checkType(function () {})); //function
```
