# 상속

### 상속\(inheritance\)이란?

* 객체는 연관된 로직들로 이루어진 작은 프로그램
* **객체의 로직을 그대로 물려 받는 또 다른 객체를 만들 수 있는 기능**
* 기존의 로직을 수정하고 변경해서 파생된 **새로운 객체를 만들 수 있게 해줌**

```javascript
function Person(name){
    this.name = name;
    this.introduce = function(){
        return 'My name is '+this.name; 
    }   
}
var p1 = new Person('egoing');
document.write(p1.introduce()+"<br />"); // My name is egoing
```

```javascript
function Person(name){
    this.name = name;
}
Person.prototype.name = null;  
Person.prototype.introduce = function(){
    return 'My name is '+this.name; 
}
var p1 = new Person('egoing');
document.write(p1.introduce()+"<br />"); // My name is egoing
```

* Programmer가 Person의 기능을 상속
* **부모의 기능을 계승 발전할 수 있는 것이 상속의 가치**
* Programmer는 Person의 기능을 가지고 있으면서 Person이 가지고 있지 않은 기능인 메소드 coding을 가지고 있음 

```javascript
function Person(name){
    this.name = name;
}
Person.prototype.name=null;
Person.prototype.introduce = function(){
    return 'My name is '+this.name; 
}
 
function Programmer(name){
    this.name = name;
}
Programmer.prototype = new Person();
Programmer.prototype.coding = function(){
    return "hello world";
}
 
var p1 = new Programmer('egoing');
document.write(p1.introduce()+"<br />"); // My name is egoing
document.write(p1.coding()+"<br />"); // hello world
```

