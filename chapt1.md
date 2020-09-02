# 숫자와 문자

### **데이터 형 \(data type\) : 숫자**

* 자바스크립트에서는 큰따옴표, 작은따옴표가 붙지 않은 숫자는 숫자로 인식
* 사칙연산 - 곱하기 : **\* \(에스터리스크\)** 사용, 나누기 : **/ \(슬래쉬\)** 사용
* 사칙연산 보다 좀 더 복잡한 연산도 **Math** 객체 사용

```javascript
Math.pow(3,2);         // 9, 3의 2승 
Math.round(10.6);      // 11, 10.6을 반올림 
Math.ceil(10.2);       // 11, 10.2를 올림 
Math.floor(10.6);      // 10, 10.6을 내림 
Math.sqrt(9);          // 3, 3의 제곱근 
Math.random();         // 0부터 1.0사이의 랜덤한 숫자

Math.round(100 * Math.random()); // 100.0사이의 반올림된 랜덤한 숫자
```

### 데이터 형 \(data type\) : 문자\(String\)

* 문자는 **"\(큰 따옴표\) , '\(작은 따옴표\)** 중의 하나로 감싸야함
* 끝날때도 시작한 따옴표로 동일하게 끝나야함
* 숫자를 따옴표로 감싸면 문자
* **typeof** : 데이터 형을 알려줌

```javascript
alert(typeof "1"); // string, 문자 
alert(typeof 1);   // number, 숫자
```

* **escape \(이스케이프\)** : \' 문자로 해석하도록 강제 할 수 있음

```javascript
alert('egoing\'s javascript'); // egoing's javascript
```

* **\n** : 줄바꿈을 의미하는 특수한 문자

```javascript
alert("coding \n everybody");
/*
    coding
    everybody
*/
```

* 문자와 문자를 더할 때 : **"문자" + "문자"**

```javascript
alert("coding"+" everybody"); // coding everybody
```

* 문자의 길이를 구할 때 : **"문자".length**

```javascript
alert("coding everybody".length); // 16
```

