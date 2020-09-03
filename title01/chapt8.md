# 배열

* 연관된 데이터를 모아서 통으로 관리하기 위한 데이터 타입
* 여러 개의 데이터를 하나의 변수에 저장 

### 배열의 생성

* 대괄호**\(\[\]\)**는 배열을 만드는 기호
* 대괄호 안에 **데이터를 콤마\(,\)로 구분**해서 나열
* **원소** : 각각의 데이터

```javascript
var member = ['egoing', 'k8805', 'sorialgi'];
```

* 배열에 담겨있는 값을 가져올 때 대괄호 안에 숫자를 넣음
* **색인** : 대괄호 안에 숫자, 0부터 시작

```javascript
var member = ['egoing', 'k8805', 'sorialgi']
alert(member[0]); // 색인 : 0, return : egoing
alert(member[1]); // 색인 : 1, return : k8805
alert(member[2]); // 색인 : 2, return : sorialgi
```

### 배열의 제어

* 데이터의 추가/수정/삭제와 같은 다양한 기능을 가지고 있음

**배열의 크기 \(length\)**

```javascript
var arr = [1, 2, 3, 4, 5];
alert(arr.length); // 5
```

### 배열의 조작

 **push 추가** 

* 배열의 **끝에 원소를 추가**
* 인자로 전달된 값을 배열\(li\)에 추가하는 명령

```javascript
var li = ['a', 'b', 'c', 'd', 'e'];
li.push('f');
alert(li); // return : a,b,c,d,e,f
```

**concat 추가** 

* **복수의 원소를 배열에 추가**
* 인자로 전달된 값을 추가하는 명령

```javascript
var li = ['a', 'b', 'c', 'd', 'e'];
li = li.concat(['f', 'g']);
alert(li); // return : a,b,c,d,e,f,g
```

**unshift 추가** 

* 배열의 **시작점에 원소 추가**
* 인자로 전달한 값을 배열의 첫번째 원소로 추가, 기존 값들의 색인을 1씩 증가

```javascript
var li = ['a', 'b', 'c', 'd', 'e'];
li.unshift('z');
alert(li); // return : z,a,b,c,d,e
```

**splice 추가** 

```javascript
splice(start, deleteCount, item);
// start : 배열에서 시작 위치
// deleteCount : start에서 지정한 시작 위치부터 삭제할 요소의 수
// item : 삭제할 위치에 추가할 요
```

```javascript
var li = ['a', 'b', 'c', 'd', 'e'];
li.splice(2, 0, 'B');
alert(li); // return : a,b,B,c,d,e
```

**shift 제거** 

* 배열의 **첫번째 원소를 제거** 

```javascript
var li = ['a', 'b', 'c', 'd', 'e'];
li.shift();
alert(li); // return : b,c,d,e
```

**pop 제거** 

* 배열의 **끝점의 원소를 배열 li에서 제거**

```javascript
var li = ['a', 'b', 'c', 'd', 'e'];
li.pop();
alert(li); // return : a,b,c,d
```

**sort 정렬** 

* **순차적으로 정렬**

```javascript
var li = ['c', 'e', 'a', 'b', 'd'];
li.sort();
alert(li); // return : a,b,c,d,e
```

**reverse 정렬** 

* **역순으로 정렬**

```javascript
var li = ['c', 'e', 'a', 'b', 'd'];
li.reverse();
alert(li); // return : d,b,a,e,c
```



