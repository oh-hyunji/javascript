# 반복문

### 반복문의 문법

**while**

* while문 뒤에 따라오는 괄호 안의 조건이 참\(true\)면 중괄호 안의 코드 구간을 반복적 실행
* 거짓\(false\)면 실되지 않음
* 종료 조건이 잘못될 경우 무한반복 또는 반복문이 실행되지 않음

```javascript
var i = 0;
// 종료조건으로 i의 값이 10보다 작다면 true, 같거나 크다면 false가 된다.  
while(i < 10){
    // 반복이 실행될 때마다 coding everybody <br/>이 출력된다. 
    // <br/> 줄바꿈을 의미하는 HTML 태그
    document.write('coding everybody <br />');
    i++; // i의 값이 1씩 증가한다. (i = i + 1;)
}

// 조건이 true일 경우는 무한루프 조심!
// 조건이 false일 경우는 실행안됨  
```

**for**

```text
for(초기화; 반복조건; 반복이 될 때마다 실행되는 코드){
    반복해서 실행될 코드
}
```

```javascript
for(var i = 0; i < 10; i++){
    document.write('coding everybody'+i+'<br />');
}

// coding everybody 9까지 return
```

### 반복문의 제어

**break**

* 반복작업을 중단 시킬때 사용
* 반복문 안에서 **break가 실행되면 반복문을 즉시 종료**

```javascript
for(var i = 0; i < 10; i++){
    if(i === 5) {
        break;
    }
    document.write('coding everybody'+i+'<br />');
}

// coding everybody 5부터는 제외하고 4까지 return
```

**continue**

* **실행을 즉시 중단 하면서 반복은 지속**됨

```javascript
for(var i = 0; i < 10; i++){
    if(i === 5) {
        continue;
    }
    document.write('coding everybody'+i+'<br />');
}

// coding everybody 5 제외하고 9까지 return
```

### 반복문의 중첩

* **for안에 for**

```javascript
// 0부터 9까지 변수 i에 순차적으로 값을 할당        
for(var i = 0; i < 10; i++){
    // 0부터 9까지의 변수를 j의 값에 순차적으로 할당
    for(var j = 0; j < 10; j++){    
        // i와 j의 값을 더한 후에 출력
        // String은 숫자인 i와 j의 데이터 타입을 문자로 형태를 변환하는 명령이다. 
        // String()을 제거하고 실행해보면 의미가 좀 더 분명하게 드러날 것이다.
        document.write(String(i)+String(j)+'<br />');
    }
}
```

