## variable scope and closure

### 코드 블록 '{}'

- code block 안에서 선언한 변수는 블록 안에서만 사용할 수 있다. 이런 특징은 특정 작업을 수행하는 코드를 한데 묶어두는 용도로 활용할 수 있다. 블록 안에는 작업 수행에만 필요한 변수가 선언된다.

- code block을 사용하는 if, for, while 등의 statement에서도 마찬가지로 '{}'안에서 선언한 변수는 오직 '{}' 안에서만 접근 가능하다.

- for의 '()'에서 선언한 변수는 '{}'안에서 선언한 변수로 취급한다.

### 중첩 함수(nested function)

- 중첩 함수는 함수 내부에서 선언한 함수를 의미한다.

- 중첩 함수는 새로운 객체의 프로퍼티 형태나 중첩 함수 그 자체로 반환될 수 있다. 반환된 중첩 함수는 어디서든 호출해 사용할 수 있다. 반환된 중첩 함수는 외부 변수에 접근할 수 있다.

## 렉시컬 환경(lexical environment)

- lexical environment는 실행 중인 함수, 코드 블록, 스크립트 전체가 갖는 내부 숨김 연관 객체(internal hidden associated object)이다.

- lexical environment는 environment record(환경 레코드)와 outer lexical environment(외부 렉시컬 환경)이라는 두 부분으로 구성된다.

- environment record는 모든 지역 변수를 프로퍼티로 저장하고 있는 객체다. 'this' 값과 같은 기타 정보도 여기에 저장된다.

- outer lexical environment는 외부의 lexical environment를 의미한다.

- 변수는 특수 내부 객체인 environment record의 프로퍼티다. 변수를 가져오거나 수정하는 것은 환경 레코드의 프로퍼티를 가져오거나 변경하는 것을 위미한다.

- global lexical environment(전역 렉시컬 환경)는 스크립트 전체와 관련된 환경을 의미한다.

- global lexical environment는 외부 참조를 갖지 않는다.

- 스크립트가 시작되면 스크립트 내에서 선언한 변수 전체가 lexical environment에 올라간다(pre-populated). 이때 변수의 상태는 특수 내부 상태(special internal state)인 'uninitialized'가 된다. 자바스크립트 엔진은 uninitialized 상태의 변수를 인지하긴 하지만 let을 만나기 전까지 해당 변수를 참조할 수 없다.

- let을 만나면 참조가 가능해지고 값을 할당하기 전에는 undefined값이 할당 된다.

- 렉시컬 환경은 명세서에서 자바스크립트가 어떻게 동작하는지 설명하는 데 쓰이는 이론상의 객체이다. 코드를 사용해 직접 렉시컬 환경을 얻거나 조작하는 것을 불가능하다.

- 자바스크립트 엔진들은 명세서에 언듭된 사항을 준수하면서 엔진 고유의 방법을 사용해 렉시컬 환경을 최적화한다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 6.3 변수 유효 범위와 클로저](https://ko.javascript.info/closure)