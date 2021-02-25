# node-js

<br>

Node.js api 공식 문서: https://nodejs.org/dist/latest-v12.x/docs/api/ <br><br>
Airbnb javascript 스타일 가이드: https://github.com/airbnb/javascript <br><br>
Google javascript 스타일 가이드: https://google.github.io/styleguide/jsguide.html

<br>


![image](https://user-images.githubusercontent.com/32799078/109110407-6b9b7e00-777a-11eb-979c-6f10b73836ae.png)

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

#### EventEmitter 객체:  
https://nodejs.org/api/events.html#events_class_eventemitter

#### Event Loop: 
https://nodejs.org/en/docs/guides/event-loop-timers-and-nexttick/ <br>
https://nodejs.org/en/docs/guides/dont-block-the-event-loop/ 




<br><br>

## web server

- 특정 프로토콜로 통신을 하는 서버 프로그램은 특정 포트 번호를 사용하도록 정해져 있다. -> 다른 포트 번호를 사용하는 해도 기술적으로는 문제가 없지만 약속이니까 지키자
- 포트 번호를 생략해도 맨 앞의 http, https 같은 프로토콜 정보를 보고 브라우저는 자동으로 그에 맞는 포트 번호를 설정하고 서버에 접속을 시도한다. 

![image](https://user-images.githubusercontent.com/32799078/109052649-3281f000-771f-11eb-971f-fdf589919b15.png)


                 
