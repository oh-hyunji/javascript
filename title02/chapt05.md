# 함수의 호출

* func는 **Function이라는 객체의 인스턴스**
* func는 객체 Function이 가지고 있는 **메소드들을 상속**
* 메소드는 **Function.apply**과 **Function.call**

```javascript
function func(){
}
func(); 
```

* sum은 Function 객체의 인스턴스로, **Function 의 메소드 apply를 호출** 

**apply** 

* 메소드는 **두개의 인자**를 가질 수 있음
* 배열의 담겨있는 원소가 함수\(sum\)의 인자로 **순차적으로 대입**
* Function.call은 사용법이 거의 비슷
* apply의 첫번째 인자로 **null**을 전달하면 **apply가 실행된 함수 인스턴스는 전역객체\(브라우저에서는 window\)를 맥락으로 실행**

```javascript
function sum(arg1, arg2){
    return arg1 + arg2;
}
alert(sum.apply(null, [1,2])) // return : 3
```

* JavaScript에서 **함수는 독립적인 객체**로서 존재하고, **apply나 call 메소드를 통해서 다른 객체의 소유물인 것처럼 실행**할 수 있

```javascript
o1 = {val1:1, val2:2, val3:3}
o2 = {v1:10, v2:50, v3:100, v4:25}
function sum(){
    var _sum = 0;
    for(name in this){
        _sum += this[name];
    }
    return _sum;
}
alert(sum.apply(o1)) // 6
alert(sum.apply(o2)) // 185
```

