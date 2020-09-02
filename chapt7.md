# 함수

* 하나의 로직을 재실행 할 수 있도록 함
* 코드의 재사용성을 높여줌

### 함수의 형식

```javascript
function 함수명( [인자...[,인자]] ){
   코드
   return 반환값
}
```

### 함수의 정의와 호출

* function 뒤에 함수의 이름이 오고 \(\)소괄호가 따라옴 
* **\(\)소괄호에 인자라는 값이 차례로 들어옴** 
* 인자 값은 함수를 호출할 때 함수의 로직으로 전달될 변수

```javascript
function numbering(){
    i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }   
}
numbering(); // return : 0 ~ 9
```

### 입력과 출력

* **입력된 값을 연산해 출력하는 것**이 함수의 기본적 역할

**return**

* return 뒤에 따라오는 값을 **함수의 결과**로 반환
* 함수를 **종료**시킴

```javascript
function get_member1(){
    return 'egoing';
}
 
function get_member2(){
    return 'k8805';
}
 
alert(get_member1()); // return : egoing
alert(get_member2()); // return : k88805

function get_member(){
    return 'egoing'; // return 여기서 종료됨
    return 'k8805';
    return 'sorialgi';
}
alert(get_member()); // return : egoing 실행 후 종료
```

**인자\(argument\)**

* **함수로 유입되는 입력 값**
* 함수가 변환하는 값이나 메소드 동작방법을 다르게 함

```javascript
function get_argument(arg){
    return arg;
}
 
alert(get_argument(1)); // 인자 : 1, return : 1 
alert(get_argument(2)); // 인자 : 2, return : 2
```

###  복수의 인자

*  여러개의 인자 값을 받는 경

```javascript
function get_arguments(arg1, arg2){
    return arg1 + arg2
}
 
alert(get_arguments(10, 20)); // 복수 인자 : 10, 20 | return : 30 
alert(get_arguments(20, 30)); // 복수 인자 : 20, 30 | return : 50 
```

### 함수를 정의 하는 다른 방법

* **함수의 표현식**

```javascript
var numbering = function (){
    i = 0;
    while(i < 10){
        document.write(i);
        i += 1;
    }   
}
numbering(); // return : 0 ~ 9
```

