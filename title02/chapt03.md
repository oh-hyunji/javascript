# 클로저

* **내부함수가 외부함수의 맥락\(context\)에 접근**할 수 있는 것

### 내부함수

* 자바스크립트는 **함수 안에서 또 다른 함수를 선언** 할 수 있음
* **내부함수는 외부함수의 지역변수에 접근**할 수 있다

```javascript
function outter(){ // 외부 함수
    var title = 'coding everybody'; 
    function inner(){ // 내부 함수 
        alert(title); // return : coding everybody - 외부함수 변수 접
    }
    inner();
}
outter();
```

### 클로저

* **내부함수와 밀접한 관계**를 가지고 있음
* **매커니즘 클로저** : 내부함수는 외부함수의 지역변수에 접근 할 수 있는데 외부함수의 실행이 끝나서 **외부함수가 소멸된 이후에도 내부함수가 외부함수의 변수에 접근**
* **내부함수가 외부함수의 지역변수에 접근** 
* 외부함수는 **외부함수의 지역변수를 사용하는 내부함수가 소멸될 때까지 소멸되지 않음** 
* 클로저의 특성을 이용해서 **Private한 속성**을 사용할 수 있음

{% hint style="info" %}
Private 속성은 객체의 외부에서는 접근 할 수 없는 외부에 감춰진 속성이나 메소드를 의미, 이를 통해서 객체의 내부에서만 사용해야 하는 값이 노출됨으로서 생길 수 있는 오류를 줄일 수 있음 
{% endhint %}

```javascript
function factory_movie(title){
    return {
        get_title : function (){
            return title;
        },
        set_title : function(_title){
            title = _title
        }
    }
}
ghost = factory_movie('Ghost in the shell');
matrix = factory_movie('Matrix');
 
alert(ghost.get_title()); // Ghost in the shell 
alert(matrix.get_title()); // Matrix 
 
ghost.set_title('공각기동대');
 
alert(ghost.get_title()); // 공각기동대 
alert(matrix.get_title()); // Matrix 
```

* **함수가 함수 외부의 컨텍스트에 접근** 

```javascript
var arr = []
for(var i = 0; i < 5; i++){
    arr[i] = function(id) {
        return function(){
            return id;
        }
    }(i);
}
for(var index in arr) {
    console.log(arr[index]());
}
/*
    0
    1
    2
    3
    4
*/
```

### 클로저 참고

* [https://developer.mozilla.org/ko/docs/JavaScript/Guide/Closures](https://developer.mozilla.org/ko/docs/JavaScript/Guide/Closures)
* [http://ejohn.org/apps/learn/\#48](http://ejohn.org/apps/learn/#48)
* [http://blog.javarouka.me/2012/01/javascripts-closure.html](http://blog.javarouka.me/2012/01/javascripts-closure.html)

