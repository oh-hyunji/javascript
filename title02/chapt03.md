# 클로저
* 내부함수가 외부함수의 맥락(context)에 접근할 수 있는 것


내부함수
* 자바스크립트는 함수 안에서 또 다른 함수를 선언 할 수 있음

클로저
* 내부함수와 밀접한 관계를 가지고 있음
* 매커니즘 클로저 : 내부함수는 외부함수의 지역변수에 접근 할 수 있는데 외부함수의 실행이 끝나서 외부함수가 소멸된 이후에도 내부함수가 외부함수의 변수에 접근
* 내부함수가 외부함수의 지역변수에 접근 
* 외부함수는 외부함수의 지역변수를 사용하는 내부함수가 소멸될 때까지 소멸되지 않는 특성

클로저 참고
* https://developer.mozilla.org/ko/docs/JavaScript/Guide/Closures
* http://ejohn.org/apps/learn/#48
* http://blog.javarouka.me/2012/01/javascripts-closure.html
