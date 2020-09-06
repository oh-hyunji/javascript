# this

* 함수 내에서 **함수 호출 맥락\(context\)**를 의미
* 함수를 어떻게 호출하느냐에 따라서 **this가 가리키는 대상이 달라짐**
* **함수와 객체**의 관계가 느슨한 자바스크립트에서 this는 **연결시켜주는 연결점** 

### 함수호출

* **this는 전역객체인 window와 같음**

```javascript
function func(){
    if(window === this){
        document.write("window === this");
    }
}
func(); // window === this
```

### 메소드의 호출

* 객체의 소속인 메소드의 **this는 그 객체를 가르킴**

```javascript
var o = {
    func : function(){
        if(o === this){
            document.write("o === this");
        }
    }
}
o.func(); // o === this
```

### 생성자의 호출

* 함수를 호출했을 때와 new를 이용해서 생성자를 호출했을 때의 차이
* **생성자는 빈 객체를 만듦** 그리고 **객체내에서 this는 만들어진 객체를 가르킴**
* 생성자가 실행되기 전까지는 객체는 변수에도 할당될 수 없기 때문에 this가 아니면 객체에 대한 어떠한 작업을 할 수 없기 때문

```javascript
var funcThis = null; 

function Func(){
    funcThis = this;
}

var o1 = Func();
if(funcThis === window){
    document.write('window <br />');
}
 
var o2 = new Func();
if(funcThis === o2){
    document.write('o2 <br />');
}

/*
    window 
    o2
*/
```

### apply, call

* **this의 값을 제어**

```javascript
var o = {}
var p = {}
function func(){
    switch(this){
        case o:
            document.write('o<br />');
            break;
        case p:
            document.write('p<br />');
            break;
        case window:
            document.write('window<br />');
            break;          
    }
}
func();
func.apply(o);
func.apply(p);

/*
    window
    o
    p
*/
```

