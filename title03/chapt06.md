# prototype

* **객체의 원형, 특수한 프로퍼티** 
* 함수는 객체 그러므로 생성자로 사용될 함수도 객체

```javascript
function Ultra(){}
Ultra.prototype.ultraProp = true;
 
function Super(){}
Super.prototype = new Ultra();
 
function Sub(){}
Sub.prototype = new Super();
 
var o = new Sub();
console.log(o.ultraProp); // true
```

**prototype chain**

* **객체와 객체를 연결하는 체인**의 역할

{% hint style="danger" %}
**Super.prototype = Ultra.prototype 으로하면 안됨**, 이렇게하면 Super.prototype의 값을 변경하면 그것이 Ultra.prototype도 변경, Super.prototype = new Ultra\(\);는 Ultra.prototype의 원형으로 하는 객체가 생성되기 때문에 new Ultra\(\)를 통해서 만들어진 객체에 변화가 생겨도 Ultra.prototype의 객체에는 영향을 주지 않음 
{% endhint %}

