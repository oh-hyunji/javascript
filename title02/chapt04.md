# arguments

* 함수에는 **arguments라는 변수에 담긴 숨겨진 유사 배열**이 있음
* 이 배열에는 함수를 호출할 때 입력한 인자가 담겨있음
* 함수안에서 사용할 수 있도록 그 이름이나 특성이 약속된 **일종의 배열**
* **arguments.length** : 함수로 전달된 인자의 개수
* 반복문을 결합하면 함수로 전달된 인자의 값을 순차적으로 가져올 수 있음

```javascript
function sum(){
    var i, _sum = 0;    
    for(i = 0; i < arguments.length; i++){
        document.write(i+' : '+arguments[i]+'<br />');
        _sum += arguments[i];
    }   
    return _sum;
}
document.write('result : ' + sum(1,2,3,4)); // result : 10
```

{% hint style="info" %}
arguments는 사실 배열이 아닌 arguments 객체의 인스턴스 
{% endhint %}

### 매개변수의 수

* **arguments.length** : 함수로 전달된 실제 인자의 수
* **함수.length** : 함수에 정의된 인자의 수

```javascript
function zero(){
    console.log(
        'zero.length', zero.length,
        'arguments', arguments.length
    );
}
function one(arg1){
    console.log(
        'one.length', one.length,
        'arguments', arguments.length
    );
}
function two(arg1, arg2){
    console.log(
        'two.length', two.length,
        'arguments', arguments.length
    );
}
zero(); // zero.length 0 arguments 0 
one('val1', 'val2');  // one.length 1 arguments 2 
two('val1');  // two.length 2 arguments 1
```



