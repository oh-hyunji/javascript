# 재귀함수

* **함수 자신을 호출하는 프로그래밍 기법**
* **팩토리얼 예시**
* 단점 :  호출 스택이 너무 커져서 메모리를 엄청나게 소비할 수 있음

```javascript
// 다른 문서 참조
function factorial (n) {
    if (n === 1) { // Base case, Termination case
        return 1;
    }
    return n * factorial(n - 1);
}
factorial(3); // 6
```

**참고**

* [http://opentutorials.org/module/904/6700](http://opentutorials.org/module/904/6700) 

