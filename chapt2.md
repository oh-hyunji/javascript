# 변수

* \(문자, 숫자 같은\) 값을 담는 컨테이너로 값을 유지할 필요가 있을 때 사용
* 변수에 담긴 값은 다른 값으로 바꿀 수 있음

### 변수의 선언

* 변수는 **var로 시작** \(권장사항\)
* **var** : 변수를 선언하겠다는 의미
* var을 생략 할 수 있지만 **유효범위**라는 것에 영향을 미침
* 변수의 이름은 $, \_, 특수 문자를 제외한 모든 문자로 시작 가능

```javascript
var a = 1;
alert(a+1);  // 2

var a = 2;
alert(a+1);  // 3

var first = "coding";
alert(first + " everybody"); // first everybody

var a = 'coding', b = 'everybody';
alert(a); // coding
alert(b); // everybody
```

* 변수는 코드의 **재활용성**을 높여줌

```javascript
// 변할 수 있는
var a = 100; 

// 변할 수 없는
a = a + 10;
alert(a); // 110

a = a / 10;
alert(a); // 11

a = a - 10; 
alert(a); // 1

a = a * 10;      
alert(a); // 10
```

