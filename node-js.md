# node-js

<br>

Node.js api 공식 문서: https://nodejs.org/dist/latest-v12.x/docs/api/

<br>

## 모듈 내부의 것을 외부에 공개하는 방법

1. 공개하고 싶은 것들을 **하나씩 exports**로 공개

2. 공개하고 싶은 것들을 모아서 **하나의 객체**로 만들고 **module.exports로 객체를 통째**로 공개

<br>

## javascript 함수 선언

#### Function Declaration(함수 선언식)

```
function add(a, b) {
  return a + b;
}
```

#### Function Expression(함수 표현식)

```
const add = function(a, b) {
  return a + b;
};
```
```
const add = (a, b) => { 
  return a + b;
};
```

<br>

## 비동기 실행

특정 작업이 완료되었을 때 실행할 **콜백**을 등록해두고 바로 **다음 코드로 실행**을 넘기는 것

Node.js의 비동기 실행은 libuv라는 라이브러리를 통해서 이루어진다. http://docs.libuv.org/en/v1.x/design.html


<br>

#### EventEmitter 객체 https://nodejs.org/api/events.html#events_class_eventemitter
