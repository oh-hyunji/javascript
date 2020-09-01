# 조건문

* 주어진 조건에 따라서 어플리케이션이 다르게 동작

## 조건문의 문법

**if**

* if로 시작 뒤에 \(\)괄호 조건이 오고, 조건이 될 수 있는 값은 Boolean
* **if문의 조건이 참이면 중괄호의 시작\({}부터 중괄호의 끝\(}\)까지의 구간이 실행**, 거짓이면 실행되지 않음.

```javascript
if(true){
    alert(1);
    alert(2);
    alert(3);
    alert(4);
}
alert(5);

// true ? return 1,2,3,4
// false ? return 5
```

**else**

* 주어진 **조건이 거짓**일 때 실행할 구간을 정의

```javascript
if(true) {
    alert(1);
} else {
    alert(2);
}

// true ? return 1 
// false ? return 2
```

**else if**

* 다양한 케이스의 조건을 검사
* if나 else와는 다르게 여러개가 올 수 있다는 점
* **else if의 모든 조건이 false라면 else가 실행**, else 생략 가능

```javascript
if(false) {
    alert(1);
} else if(false) {
    alert(2);
} else if(true) {
    alert(3);
} else {
    alert(4);
}

// return 3
// 다 false일 경우 return 4
```

## 변수와 비교연산자

**prompt\(\)** : 사용자가 입력한 값을 가져와서 id 변수의 값으로 대입 API, 함수라고 함

* id가 name이면 '아이디가 일치 합니다' 출력

```javascript
id = prompt('아이디를 입력해주세요.');

if(id == 'name') { 
    // 입력받은 값이 name이면 실행
    alert('아이디가 일치 합니다.'); 
} else {
    alert('아이디가 일치하지 않습니다.');
}
```

## 조건문의 중첩

* if문 안에 if문이 등장 

```javascript
id = prompt('아이디를 입력해주세요.');

if(id == 'name') {
    password = prompt('비밀번호를 입력해주세요.');
    if(password === '111111'){ // if안 if 중첩문  
        alert('인증 했습니다.');
    } else {
        alert('인증에 실패 했습니다.');
    }
} else {
    alert('인증에 실패 했습니다.');
}
```

## 논리 연산자

**&& \(and 연산자\)**

* 좌항과 우항이 **모두 true\(참\)**일 때 참
* 중첩 if문을 줄일 수 있음, 코드의 복잡성이 낮아짐

```javascript
id = prompt('아이디를 입력해주세요.');
password = prompt('비밀번호를 입력해주세요.');

// 조건문 중첩 사용하시 않고 and 연산자 사용
if(id == 'egoing' && password == '111111'){
    alert('인증 했습니다.'); // 조건 성립
} else {
    alert('인증에 실패 했습니다.');
}
```

**\|\| \(or 연산자\)**

* 좌항과 우항 둘중 **하나가 true**면 true가 됨
* 좌항, 우항 모두 false면 false

```javascript
id = prompt('아이디를 입력해주세요.');
password = prompt('비밀번호를 입력해주세요.');
if((id === 'egoing' || id === 'k8805' || id === 'sorialgi') && password === '111111'){
    alert('인증 했습니다.'); // 조건중 하나만 성립하면 실행  
} else {
    alert('인증에 실패 했습니다.');
}
```

**! \(not 연산자\)**

* Boolean의 값을 역전시킴

```javascript
if(!true && !true){ //  false && false
    alert(1);
}
```

## Boolean의 대체제

* **0,1** : 조건문에 사용될 수 있는 데이터 형은 불리만 되는 것이 아님

```javascript
if(0){ // false
    alert(1);
}

if(1){ // true
    alert(2);
}
```

**기타 false로 간주되는 데이터 형**

* false와 0 외에 false로 간주되는 데이터형의 리스트

```javascript
if(!''){
    alert('빈 문자열')
}

if(!undefined){
    alert('undefined');
}

var a;
if(!a){
    alert('값이 할당되지 않은 변수'); 
}

if(!null){
    alert('null');
}

if(!NaN){
    alert('NaN');
}
```

