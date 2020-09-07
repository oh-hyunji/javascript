# 참조

### 복제

* 변수 b의 값에 변수 a의 **값이 복제** 

```javascript
var a = 1;
var b = a;
b = 2;
console.log(a); // 1
```

### 참조

* 변수 b와 변수 a에 담긴 **객체가 서로 같다는 것** 
* **객체는 참조 데이터형**

```javascript
var a = {'id':1};
var b = a;
b.id = 2;

console.log(a.id);  // 2
```

### 함수

* 파라미터 b는 객체 a의 레퍼런스
* 객체를 대상으로 수정, b의 변경은 a에도 영향을 미침 

```javascript
var a = {'id':1};
function func(b){
    b.id = 2;
}
func(a);
console.log(a.id);  // 2
```

