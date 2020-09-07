# 표준 내장 객체의 확장

* Standard Built-in Object
* 자바스크립트가 **기본적으로 가지고 있는 객체**들을 의미
* 프로그래밍을 하는데 기본적으로 필요한 도구

**자바스크립트 내장 객체**

* Object
* Function
* Array
* String
* Boolean
* Number
* Math
* Date
* RegExp

### 배열을 확장

```javascript
var arr = new Array('seoul','new york','ladarkh','pusan', 'Tsukuba');
function getRandomValueFromArray(haystack){
    var index = Math.floor(haystack.length*Math.random());
    return haystack[index]; 
}
console.log(getRandomValueFromArray(arr));
```

* 함수를 배열 객체에 포함, 배열에 내장된 메소드인 것처럼 기능을 사용

```javascript
Array.prototype.rand = function(){
    var index = Math.floor(this.length*Math.random());
    return this[index];
}
var arr = new Array('seoul','new york','ladarkh','pusan', 'Tsukuba');
console.log(arr.rand());
```

