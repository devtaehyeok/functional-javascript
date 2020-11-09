### 프로그래밍 인사이트
# 함수형 자바스크립트 프로그래밍

[Yes24](http://www.yes24.com/24/Goods/56885507?Acode=101) | [알라딘](http://www.aladin.co.kr/shop/wproduct.aspx?ItemId=123715872) | [교보문고](http://www.kyobobook.co.kr/product/detailViewKor.laf?ejkGb=KOR&mallGb=KOR&barcode=9788966262120&orderClick=LEA&Kc=) | [인터파크](http://shopping.interpark.com/product/productInfo.do?prdNo=5285478131&dispNo=008001083&smid1=common_prd)

### 책 소개글
 - http://www.insightbook.co.kr/12318

### 책 미리보기
 - https://github.com/indongyoo/functional-javascript/wiki

### 책 예제 코드
 - https://github.com/indongyoo/functional-javascript/tree/master/함수형-자바스크립트-프로그래밍-책-예제

### [아티클] ES6+, 함수형 프로그래밍, 비동기, 동시성 프로그래밍
 - https://github.com/Functional-JavaScript/functional.es
 
### 인프런 동영상 강의 - 자바스크립트로 알아보는 함수형 프로그래밍
 - https://www.inflearn.com/course/함수형-프로그래밍/

### 동영상 강의 예제 코드
 - https://github.com/indongyoo/functional-javascript/tree/master/인프런-동영상-강의-예제

### 함수형 자바스크립트 라이브러리 - Partial.js
 - https://marpple.github.io/partial.js

### 함수형 자바스크립트 심플 세트 - window.functions.js
 - http://github.com/marpple/window.functions.js

호이스팅
끌어올린다
함수표현식은 선언만 끌어올린다
할당은 순서대로
선언은 그대로
함수표현식을 쓰자 (익명, 람다)
스코프 = 변수의 유효 범위 정의 시 결정
실행컨텍스트는 실행되는 코드덩어리 실행 시 결정

실행 컨텍스트에는 호이스팅, this 바인딩 등의 정보가 담긴다 
실행컨텍스트가 생길 때 호이스팅이 일어남
전역 실행컨텍스트
변수 선언도 위로 올라가고
할당은 뒤로 감...
변수선언
함수 선언 위로 올라감 !!!!
할당은 순서대로
선언은 그대로

함수와 메소드의 차이는 this를 바인딩하느냐 안하느냐 
바인딩 후 출력

객체:
배열
함수
정규표현식
객체 생성 시 주소값 할당 및 함수 선언
함수 호출 시 this에 객체 바인딩

something will call this function back
무언가가 이 함수를 돌려준다.
제어권을 넘겨준다, 맡긴다

주기함수에게 콜백함수의 제어권을 넘긴다.

메소드를 콜백으로 넘기면 함수가 된다
this가 윈도우 객체가 된다.

함수는 전역객체의 메소드다.

call
apply
bind == currying 새로운함수 생성

부수효과를 미워하고 순수함수를 만든다
외부 영향 주거나 밭지 않는다.
조합성을 강조한다 모듈화 수준을 높인다
오류를 줄이고 안정성을 높여서 생산성을 높인다.

```javascript

var obj1 ={val:10};
// 함수형 프로그래밍은 외부 값을 변형시키지 않으면서 값을 바꿔나감
function add5(obj,b){
    return {val : obj.val +b}
}

```

순수 함수의 특징

1. 항상 동일한 인자 동일한 결과
2. 평가 시점이 중요하지 않음 -> 함수형 프로그래밍이 가능한 이유 조합성 강조
3. 
스레드와 상관없이...
에드 결과를 인풋으로 넘기든...

자바스크립트 함수 일급함수
함수가 객체로 (값으로) 다루어질 수 있음
함수를 변수에 담고 인자로 넘기고 다른 함수가 실행

자바스크립트는 변수에 함수가 담길 수 있다.

함수가 함수를 인자로 받을 수 있다

언제 평가해도 상관 없는 순수함수를 많이 만들고
들고다니면서 항상 평가


```javascript

// 일급 객체
// 클로저
// 순수 함수 stateless 어느 시점 평가 동일 결과 동일 인자 동일 견과 
function add_maker(a){
    return function(b){
        return a+b;
    }
}

function f4(f1,f2,f3){
    return f3(f1()+f2())
}
console.log(

f4(
function(){return 2;},
function(){return 1;},
function(){return a * a}
));
```

부수 효과를 미워한다 > 순수 함수를 만든다
조합성을 강조한다 > 모듈화 수준을 높인다
순수 함수 > 외부 상태에 영향을 주고받지 않는다. 오류를 줄이고 안정성을 높인다. 평가 시점이 중요하지 않는다
모듈화 수준이 높다 > 생산성을 높인다

재미 / 실시간성 : 라이브방송, 실시간댓글, 협업, 메신저
독창성 / 완성도 : 애니메이션, 무한스크롤 ,벽돌
더 많아져야 하는 동시성 : 비동기 I/O, CSP, Actor, STM... 
더 빨라야 하는 반응성 / 고가용성 : ELB, Auto Scaling, OTP Supervisor 
대용량 / 정확성 / 병렬성 : MapReduce, Clojure Reducers ...
복잡도 / MSA / ... :  많아지고 세밀해지는 도구들
굉장히 세밀한 도구들을 모아서 프로그램을 만든다

스멀스멀 다가오는 FP
좋아지는 하드웨어 성능
좋아지는 컴파일러
함수형 프로그래밍 기술
좋아지는 분산 / 리액티브 환경
동시성 + 병렬성 관련 기술
성공적인 적용 사례와 영향

함수형 사고방식은 문제의 해결 방법을
동사들로 구성 함수들로 조합하는 것
함수형 프로그래밍은 언어 자체를 함수처럼 여기고 함수 개념을 가장 우선순이에 놓는다.

함수가 먼저나오면 함수형

해당 배열에 직접 필터링 하는게 아니라
새로운 배열을 만듬
if 조건을 함수에게 넘김
응용형 함수 , 적용형 프로그래밍
함수가 함수를 인자로 받아서 원하는 시점에 평가하며 해당 함수가 알고있는 인자를 적용해기며 실행

안정성 높고 테스트 쉬운 코드

```JS

// 재사용성이 높은 함수

function _filter(users,predi){
    var new_list = [];
    for (var i = 0 ; i < users.length;i++){

    }if(predi(users[i])){
        new_list.push(users[i]);
    }
    return new_list
}
function _map(users,mapper){
    var new_list = [];
    for (var i = 0 ; i < users.length;i++){
        new_list.push(mapper(list))
    }
    return new_list
}

// 30세 이상 함수형 프로그래밍
var over_30 = _filter(users,function(user){return user.age >= 30;});
var ages = _map(over_30,function(user){
    return user.age;
}));



```
