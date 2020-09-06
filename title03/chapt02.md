# 생성자와 new

### 객체

* 서로 연관된 **변수와 함수를 그룹핑한 그릇**
* 객체 내의 **변수를 프로퍼티\(property\)**, **함수는 메소드\(method\)**
* **생성자** : 객체의 구조를 재활용할 수 있는 방법

```javascript
var person = {
    'name' : 'egoing',
    'introduce' : function(){
        return 'My name is '+this.name;
    }
}
document.write(person.introduce());
```

### 생성자\(constructor\)

* **객체를 만드는 역할**을 하는 함수
* 함수는 재사용 가능한 로직의 묶음이 아니라 **객체를 만드는 창조자**
* 함수를 호출할 때 **new을 붙이면 새로운 객체를 만든 후에 이를 리턴**
* 생성자 함수는 일반함수와 구분하기 위해서 **첫글자를 대문자**로 표시

```javascript
function Person(name){
    this.name = name;
    this.introduce = function(){
        return 'My name is '+this.name; 
    }   
}
var p1 = new Person('egoing');
document.write(p1.introduce()+"<br />");
 
var p2 = new Person('leezche');
document.write(p2.introduce());
```

### 자바스크립트 생성자의 특징

* **객체를 만드는 주체는 함수**
* 함수에 **new를 붙이는 것을 통해** 객체를 만들 수 있음 
* 자바스크립트가 추구하는 **자유로움을 보여주는 사례**

