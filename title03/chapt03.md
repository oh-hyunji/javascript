# 전역객체

### 전역객체란?

* **전역객체\(Global object\)는 특수한 객체**
* 전역변수와 함수는 사실 window 객체의 프로퍼티
* 객체를 명시하지 않으면 암시적으로 window의 프로퍼티로 간주

```javascript
function func(){
    alert('Hello?');    
}
func();
window.func();

// func();와 window.func();는 모두 실행
```

* **모든 객체는 기본적으로 전역객체의 프로퍼티** 

```javascript
var o = {'func':function(){
    alert('Hello?');
}}
o.func();
window.o.func();
```

### 전역객체 API

* ECMAScript에서는 전역객체의 [API](http://opentutorials.org/course/50/44)를 정의
* 그 외의 API는 호스트 환경에서 필요에 따라서 추가로 정의
* 웹브라우저 자바스크립트에서는 alert\(\)이라는 전역객체의 메소드가 존재
* 웹브라우저에서 전역객체는 window

