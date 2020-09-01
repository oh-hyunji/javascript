# 비교

### 비교 연산자

* 결과는 true\(참\)나 false\(거짓\) 중 하나
* true, false 는 블린\(boolean\) 데이터 형식 

**대입 연산자 \(=\)**

```text
a=1 // '='는 우항의 값 1을 좌항의 변수 a에 대입
```

**동등 연산자 \(==\)**

* 좌항과 우항을 비교해 서로 값이 같으면 true, 다르면 false

**일치 연산자 \(===\)**

* 좌항과 우항이 '정확'하게 같으면 true, 다르면 false
* 서로 같은 수를 표현하고 있더라도 데이터 형이 같은 경우에만 같다고 판단
* **동등 연산자 보다 일치 연산자 사용을 권장함**

```text
alert(1=='1');   // true
alert(1==='1');  // false : 데이터형 다름
```

**null** : 값이 없음을 명시적으로 표시 

**undefined** : 그냥 값이 없는 상태 

**NaN** : 0/0과 같은 연산의 결과로 만들어지는 특수한 데이터 형인데 숫자가 아님

```text
alert(null == undefined);       // true
alert(null === undefined);      // false
alert(true == 1);               // true
alert(true === 1);              // false
alert(true == '1');             // true
alert(true === '1');            // false
 
alert(0 === -0);                // true
alert(NaN === NaN);             // false
```

**!=** : 같지 않음 , **!==** : 정확하게 같지 않 

```text
alert(1!=2);            // true
alert(1!=1);            // false
alert("one"!="two");    // true
alert("one"!="one");    // false

alert(1!=='1');         // true
alert(1!==1);           // false
```

**&gt;**

* 좌항이 우항보다 크다면 참, 아니면 거짓
* &lt; 반대의 의미

**&gt;=**

* 좌항이 우항보다 크거나 같음
* &lt;= 반대의 의미

```text
alert(10>20);   // false
alert(10>1);    // true
alert(10>10);   // false

alert(10>=20);  // false
alert(10>=1);   // true
alert(10>=10);  // true
```

