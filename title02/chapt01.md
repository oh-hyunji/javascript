# 유효범위

* Scope - 변수의 수명, 유효범위

**전역변수**

* **함수 밖에서 변수를 선언**한 변수
* 애플리케이션 전역에 접근이 가능한 변수
* **어떤 함수 안에서도 그 변수에 접근** 할 수 있음
* **사용지 않는 것이 좋음,** 값이 변경될 수 있고 함수의 동작이 달라질 수 있음
* 사용시 이유를 명확히 알고 있어야 함

**지역변수**

* **함수 안에서만 접근** 가능
* 같은 이름의 지역변수, 전역변수가 동시에 정의되면 **지역변수가 우선**함
* **var를 사용하지 않은 지역변수는 전역변수가 됨**

```javascript
var vscope = 'global'; // 전역변수
function fscope(){
    vscope = 'local'; // var 있으면 지역변수 없으면 전역변
    alert('함수안'+vscope); // return : local
}
fscope();
alert('함수밖'+vscope); // return : local
```

### 유효범위의 효용

**지역변수의 사용**

```javascript
function a (){
    var i = 0;
}
for(var i = 0; i < 5; i++){
    a();
    document.write(i);
}

// return : 01234
```

**전역변수의 사용**

```javascript
function a (){
    i = 0; // var가 없
}
for(i = 0; i < 5; i++){
    a();
    document.write(i);
}

// 무한반
```

### 전역변수의 사용

* **하나의 객체를 전역변수로 만들고 객체의 속성으로 변수를 관리**하는 방법 사용 

```javascript
MYAPP = {}
MYAPP.calculator = {
    'left' : null,
    'right' : null
}
MYAPP.coordinate = {
    'left' : null,
    'right' : null
}
 
MYAPP.calculator.left = 10;
MYAPP.calculator.right = 20;
function sum(){
    return MYAPP.calculator.left + MYAPP.calculator.right;
}
document.write(sum());

// 전역변수를 사용하고 싶지 않다면 아래와 같이 익명함수를 호출함
(function(){ // 익명함수, 즉시실
    var MYAPP = {}
    MYAPP.calculator = {
        'left' : null,
        'right' : null
    }
    MYAPP.coordinate = {
        'left' : null,
        'right' : null
    }
    MYAPP.calculator.left = 10;
    MYAPP.calculator.right = 20;
    function sum(){
        return MYAPP.calculator.left + MYAPP.calculator.right;
    }
    document.write(sum());
}())
// 익명함수 밖에서 MYAPP 호출 안됨
```

### 유효범위의 대상 \(함수\)

* 자바스크립트는 **함수에 대한 유효범위만을 제공**
* **for문, if문 ... 안에서는 지역변수의 의미를 갖지 않음**

```javascript
for(var i = 0; i < 1; i++){
    var name = 'coding everybody';
}
alert(name);
```

### 정적 유효범위

* **함수가 선언된 시점에서의 유효범위를 갖음**
* 유효범위의 방식 : **정적 유효범위\(static scoping\),  렉시컬\(lexical scoping\)** 

```javascript
var i = 5;
 
function a(){
    var i = 10;
    b();
}
 
function b(){
    document.write(i); // 전역변수 i 참조 
}
 
a(); // retrun : 5
```

