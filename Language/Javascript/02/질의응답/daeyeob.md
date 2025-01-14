# 11. 전역 변수의 문제점

## :one: 전역 변수 사용을 억제하는 방법에는 무엇이 있는가?

<hr>

```js
(function () {
  var foo = 10; //즉시 실행함수의 지역 변수
  //..
})();

console.log(foo); // ReferenceError
```

- 모든 코드를 즉시 실행함수로 감싸서 모든 변수가 즉시 실행 함수의 지역변수가 되게 만듦

## :two: 변수의 생명 주기에 대해 설명해주세요

<hr>

- 변수가 자신이 생성된 위치에서 생성되고 소멸되기까지의 기간을 뜻함
- 전역 변수의 생명주기는 애플리케이션의 경우 생명주기와 동일하지만, 함수 내부에서 선언된 지역 변수는 함수가 호출되면 생성되고 함수가 종료되면 소멸됨

## :three: 전역 변수의 문제점에 대해 설명해주세요

<hr>

- 전역 변수는 전역 코드가 종료될 때까지 계속해서 살아있으므로 사용하지 않아도 살아있으므로 메모리가 낭비됨
- 스코프 체인 상 종점에 존재하므로 변수 검색시 가장 마지막에 검색된다. 즉, 검색 속도가 가장 늦어진다.

## :four: 전역 변수를 반드시 사용해야 할 경우에 대해 설명해주세요

<hr>

- 정석적인 대답

  - 프로그램이 실행되는 내내 변하지 않아야 하는 값이나 여러 함수에 걸쳐서 사용하는 값들은 전역 변수로 선언해서 사용하는것이 좋다. 반면에 특정 함수에서만 사용되는 값들은 지역 변수로 선언하는 것들이 좋다.

- 좋은 예시는 아님
  - 함수외부에서 선언된 전역 변수를 사용하고 싶은 경우. 이 경우, 함수 내부에서는 이 변수에 접근하기 위해 전역 변수를 사용해야함. 동일한 변수명이 함수 내부와 외부 모두에 존재할 경우, 전역변수 키워드를 사용하지 않으면 별개의 변수로 취급한다.

## :five: 네임스페이스에 대해 설명해주세요

<hr>

- 식별자간 충돌을 방지하기 위해서 스코프를 부여하는 프로그래밍 기법
- 자바스크립트에서는 기본적으로 네임스페이스를 제공하지않으나, 전역 객체를 만들어서 이 기능을 흉내낼 수 있다 (반면 타입스크립트에서는 네임스페이스 기능을 제공함 - 네임스페이스 DOM이용)

<br>

# 12. let, const 키워드와 블록 레벨 스코프

## :one: var 키워드로 선언한 전역 변수와 let 키워드로 선언한 전역 변수의 차이를 설명해주세요.

<hr>

- 답변

## :two: var보다 let, const 사용을 권장하는 이유를 설명해주세요.

<hr>

-

## :three: 일시적 사각지대(Temporal Dead Zone; TDZ)와 TDZ에 영향을 받는 구문들에 대해 설명해주세요.

<hr>

- 답변

## :four: const 키워드로 선언한 값을 변경할 수 있는 방법에 대해 설명해주세요

<hr>

- 답변

## :five: 클로저는 어떤 문제를 회피하기 위해 사용하는 방법인지 스코프를 들어 설명해주세요

<hr>

- 답변

<br>

# 13. 프로퍼티 어트리뷰트

## :one: attribute와 property의 차이점은 무엇인가요?

<hr>

- 답변

## :two: 데이터 프로퍼티와 접근자 프로퍼티에 대해 설명해주세요.

<hr>

- 답변

## :three: 객체 변경을 방지하는 메소드들에 대해 설명해주세요.

<hr>

- 답변

## :four: 자바스크립트는 내부 슬롯과 내부 메서드를 통해 접근이 가능한지에 대해 설명해주세요.

<hr>

- 답변

## :five: 프로퍼티가 생성될 때 어떠한 것들을 정의하나요?

<hr>

- 답변

<br>

# 14. 생성자 함수에 의한 객체 생성

## :one: 클래스와 생성자 함수의 차이점은 무엇인가요?

<hr>

- 답변

## :two: 객체를 생성하는 방식과 방식에 대한 문제점과 장점에 대해 설명해주세요.

<hr>

- 답변

## :three: constructor와 non-constructor 함수 객체의 차이점에 대해 설명해주세요.

<hr>

- 답변

## :four: 생성자 함수의 인스턴스 생성 과정을 설명해주세요.

<hr>

- 답변

## :five: 생성자 함수의 this 는 무엇을 의미하나요?

<hr>

- 답변

<br>

# 15. 함수와 일급 객체

## :one: 순수함수란 무엇이며, 일반함수와의 차이점은 무엇인가요?

<hr>

- 답변

## :two: 유사 배열 객체와 이터러블의 차이점에 대해 설명해주세요.

<hr>

- 답변

## :three: 일급 객체의 조건에 대해 설명해주세요.

<hr>

- 답변

## :four: arguments 프로퍼티에 대해 설명해주세요.

<hr>

- 답변

## :five: name 프로퍼티는 ES5 와 ES6 에서 어떤식으로 동작을 하나요?

<hr>

- 답변

<br>
