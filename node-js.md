# node-js

<br>

Node.js api 공식 문서: https://nodejs.org/dist/latest-v12.x/docs/api/ <br><br>
Airbnb javascript 스타일 가이드: https://github.com/airbnb/javascript <br><br>
Google javascript 스타일 가이드: https://google.github.io/styleguide/jsguide.html

<br>


![image](https://user-images.githubusercontent.com/32799078/109110407-6b9b7e00-777a-11eb-979c-6f10b73836ae.png)

1. package.json이라는 파일을 가진 디렉토리가 패키지다.
2. 하나의 서드 파티 모듈은 하나의 패키지다.
3. 서드 파티 모듈을 관리할 때 쓰는 npm은 node package manager의 줄임말이다. 

<br>

## package.json 
https://docs.npmjs.com/cli/v7/configuring-npm/package-json

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


                 
## npm

웹 프론트엔드 개발을 할 때는

(1) 코드가 잘 작동하는지를 검사하는 테스트 작업(testing)

(2) 자바스크립트 코드가 가독성 좋은 포맷으로 잘 작성되었는지를 검사하고 수정하는 작업(code formatting)

(3) 작성한 자바스크립트 코드가 자바스크립트 최신 표준을 지원하지 않는, 오래된 브라우저(특히, 인터넷 익스플로러 등)에서도 문제없이 동작할 수 있도록 변환하거나 자바스크립트의 단점을 보완한 언어(Typescript 등)로 작성한 코드를 다시 자바스크립트로 변환하는 트랜스파일 작업(transpiling)

(4) 여러 자바스크립트 파일들과 CSS 파일 등을 하나의 파일로 묶는 번들링 작업(bundling),

(5) 번들링된 결과를 더 작은 용량으로 압축해주는 작업(minifying),

(6) 이런 작업들을 한 번에 자동으로 실행할 수 있도록 설정하는 작업(Task Runner)

등이 필요하다. 개발자들은 보통 이런 작업들을 이미 공신력있는 유명 툴들을 사용해서 수행한다. 이때 각각의 작업을 수행할 수 있는 대표적인 도구들의 이름은 다음과 같다.

(1) testing 작업 - Mocha 
(2) code formatting 작업 - ESLint
(3) transpiling 작업 - Babel
(4) bundling 작업 - Webpack
(5) minifying 작업 - Uglify-JS
(6) Task Runner - Gulp

웹 프론트엔드 개발자들도 이런 툴들을 모두 npm 저장소에서 패키지로 다운로드받아 사용한다
