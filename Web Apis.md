#### console

```javascript
// .log() .warn() .error() .dir()

// 콘솔에 메시지나 객체를 출력한다.

// - log: 일반 메시지
// - warn: 경고 메시지
// - error: 에러 메시지
// - dir : 속성을 볼 수 있는 객체를 출력
```

```javascript
// .count(), .countReset()

// 콘솔에 메소드 호출의 누적 횟수를 출력하거나 초기화를 한다.

console.count("a"); // a: 1
console.count("a"); // a: 2
console.count("b"); // b: 1
console.count("a"); // a: 3
console.log("a"); // Reset a!
console.countReset("a"); // reset
console.count("a"); // a: 1
console.count("b"); // b: 2
```

```javascript
// .time(), .timeEnd()

// 콘솔에 타이머가 시작해서 종료되기까지의 시간(ms)을 출력한다.

console.time("반복문");

for (let i = 0; i < 10000; i++) {
  console.log(i); //
}

console.timeEnd("반복문"); // 10000번 동안 동작하고 얼마나 걸렸는지 출력 132.23523423ms
```

```javascript
// .trace()

// 메소드 호출 스택(call Stack)을 추적해 출력한다.

function a() {
  function b() {
    function c() {
      console.log("Log!");
      console.trace("Trace!"); // c @main.js:10 b @main.js:12 c @main.js:14
    }
    c();
  }
  b();
}
a();
```

```javascript
// .clear()

// 콘솔에 기록된 메시지를 모두 삭제한다.

console.log(1);
console.log(2);
console.log(3);
console.clear(); // 콘솔 삭제됨
```
