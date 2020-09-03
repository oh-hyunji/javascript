# 정규표현식

* 문자열에서 **특정한 문자를 찾아내는 도구**
* 특정한 조건의 문자를 **'검색'**하거나 **'치환'**하는 과정

### 정규표현식 생성

* **컴파일\(compile\), 실행\(execution\)** 두가지 단계로 이루어짐

### 컴파일

* 검출하고자 하는 패턴을 만드는 일

**정규표현식 리터럴**

```javascript
var pattern = /a/
```

**정규표현식 객체 생성자**

```javascript
var pattern = new RegExp('a'); // RegExp 객체 생
```

### 정규표현식 메소드 실행

**RegExp.exec\(\)**

```javascript
console.log(pattern.exec('abcdef')); // ["a"]
console.log(pattern.exec('bcdefg')); // null - a가 문자열에 없기 때문 
```

**RegExp.test\(\)**

* **문자열이 있으면 true, 없으면 false를 리턴** 

```javascript
console.log(pattern.test('abcdef')); // true
cnosole.log(pattern.test('bcdefg')); // false
```

### 문자열 메소드 실행

**String.match\(\)**

```javascript
// RegExp.exec()와 비슷
console.log('abcdef'.match(pattern)); // ["a"]
console.log('bcdefg'.match(pattern)); // null
```

**String.replace\(\)**

* **문자열에서 패턴을 검색해서 이를 변경한 후에 변경된 값을 리턴** 

```javascript
console.log('abcdef'.replace(pattern, 'A'));  // Abcdef
```

### 옵션

**i** 

* i를 붙이면 **대소문자를 구분하지 않음** 

```javascript
var xi = /a/;
console.log("Abcde".match(xi)); // null
var oi = /a/i;
console.log("Abcde".match(oi)); // ["A"];
```

 **g**

* g를 붙이면 **검색된 모든 결과를 리턴**

```javascript
var xg = /a/;
console.log("abcdea".match(xg)); // ["a", index: 0, input: "abcdea", groups: undefined]
var og = /a/g;
console.log("abcdea".match(og)); //  ["a", "a"]
```

###  사례

 **캡처**

* 괄호안의 **패턴은 마치 변수처럼 재사용**
* $: coding과 everybody의 순서를 역전시킨다.

```javascript
var pattern = /(\w+)\s(\w+)/;
var str = "coding everybody";
var result = str.replace(pattern, "$2, $1");
console.log(result); // everybody, coding 
```

 **치환** 

```javascript
var urlPattern = /\b(?:https?):\/\/[a-z0-9-+&@#\/%?=~_|!:,.;]*/gim;
var content = '생활코딩 : http://opentutorials.org/course/1 입니다. 네이버 : http://naver.com 입니다. ';
var result = content.replace(urlPattern, function(url){
    return '<a href="'+url+'">'+url+'</a>';
});
console.log(result);

// 생활코딩 : <a href="http://opentutorials.org/course/1">http://opentutorials.org/course/1</a> 입니다. 네이버 : <a href="http://naver.com">http://naver.com</a> 입니다.
```

###  참

*  [정규표현식을 시각화](http://www.regexper.com/)
*  [정규표현식 빌더](http://www.regexr.com/)

