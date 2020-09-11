# Object

* **객체의 가장 기본적인 형태**를 가지고 있는 객체
* 아무것도 상속받지 않는 **순수한 객체** 
* 자바스크립트의 **모든 객체는 Object 객체를 상속** 
* 모든 객체는 Object 객체의 프로퍼티를 가지고 있음 

```javascript
var grades = {'egoing': 10, 'k8805': 6, 'sorialgi': 80};
```

* Object 객체를 확장하면 모든 객체가 접근할 수 있는 **API를 만들 수 있음**
* Object 객체를 확장한 사례

```javascript
Object.prototype.contain = function(neddle) {
    for(var name in this){
        if(this[name] === neddle){
            return true;
        }
    }
    return false;
}

var o = {'name':'egoing', 'city':'seoul'}
console.log(o.contain('egoing')); // true

var a = ['egoing','leezche','grapittie'];
console.log(a.contain('leezche')); // true
```

* **Object 객체는 확장하지 않는 것이 바람직**, 모든 객체에 영향  

```javascript
for(var name in o){
    console.log(name);  
}
/*
    name
    city
    contain // 확장한 프로퍼티 
*/
```

* 프로퍼티의 객체 소속을 체크해볼 수 있는 **hasOwnProperty** 사용
* **hasOwnProperty는 인자로 전달된 속성의 이름이 객체의 속성인지 여부를 판단**, 만약 prototype으로 상속 받은 객체라면 false

```javascript
for(var name in o){
    if(o.hasOwnProperty(name))
        console.log(name);  
}
/*
    name
    city
*/
```

