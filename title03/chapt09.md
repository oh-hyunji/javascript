# 데이터 타입

* **데이터의 형태**

### 원시 데이터 타입

* **객체가 아닌 데이터 타입**
  * 숫자
  * 문자열
  * 불리언\(true/false\)
  * null
  * undefined
* 그 외의 모든 데이터 타입은 객체

### 레퍼 객체

* **String, Number, Boolean**
* **원시 데이터 형을 객체처럼 다룰 수 있도록 하기 위한 객체**
* 원시 데이터 타입과 객체는 좀 다른 동작 방법을 가지고 있음, 분별 필요 

```javascript
var str = 'coding';
str.prop = 'everybody';
console.log(str.prop);      // undefined
```

