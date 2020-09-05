# 값으로서의 함수와 콜백

* **함수도 객체**, 일종의 값
* **함수가 값이 될 수 있음**
* 객체의 속성 값으로 담겨진 함수 : **메소드\(method\)**

```javascript
a = {
    b:function(){
    }
};
```

* 함수는 값이기 때문에 **다른 함수의 인자로 전달**

```javascript
function cal(func, num){
    return func(num)
}
function increase(num){
    return num+1
}
function decrease(num){
    return num-1
}
alert(cal(increase, 1)); // return : 2
alert(cal(decrease, 1)); // return : 0
```

* 함수는 **함수의 리턴 값으로도 사용**

```javascript
function cal(mode){
    var funcs = {
        'plus' : function(left, right){return left + right},
        'minus' : function(left, right){return left - right}
    }
    return funcs[mode];
}
alert(cal('plus')(2,1)); // return : 3
alert(cal('minus')(2,1)); // return : 1
```

* 함수는 **배열 값으로도 사용**

```javascript
var process = [
    function(input){ return input + 10;},
    function(input){ return input * input;},
    function(input){ return input / 2;}
];
var input = 1;
for(var i = 0; i < process.length; i++){
    input = process[i](input);
}
alert(input); // return : 60.5
```

### 콜백 

**처리위임**

* 함수의 **인자로 함수 전달** 
* 인자로 전달된 함수 sortNumber의 구현에 따라서 sort의 동작방법이 완전히 바뀌게 됨

```javascript
function sortNumber(a,b){
    // 위의 예제와 비교해서 a와 b의 순서를 바꾸면 정렬순서가 반대가 된다.
    return b-a;
}
var numbers = [20, 10, 9,8,7,6,5,4,3,2,1];
alert(numbers.sort(sortNumber)); // array, [20,10,9,8,7,6,5,4,3,2,1]
```

**비동기처리**

* 시간이 오래걸리는 작업이 있을 때 이 작업이 완료된 후 처리해야 할 일을 **콜백으로 지정하면 해당 작업이 끝났을 때 미리 등록한 작업을 실행**할 수 있음

```javascript
// datasource.json.js
{"title":"JavaScript","author":"egoing"}

// demo1.html
$.get('./datasource.json.js', function(result){
    console.log(result);
}, 'json');
```

