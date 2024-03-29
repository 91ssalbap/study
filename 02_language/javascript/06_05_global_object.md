## global object

- 전역 객체를 사용하면 어디서나 사용 가능한 변수나 함수를 만들 수 있다.

- 전역 객체는 언어 자체나 호스트 환경에 기본 내장되어 있는 경우가 많다.

- 브라우저 환경에서는 전역객체를 window, Node js 환경에서는 global이라고 부른다.

- 전역 객체의 이름을 globalThis로 표준화하자는 내용이 최근에 자바스크립트 명세에 추가되었다.

- 브라우저에서 var로 선언한 전역 함수나 전역 변수는 전역 객체의 프로퍼티가 된다.

- const나 let을 사용하면 전역 객체를 통해 해당 변수에 접근할 수 없다.

- 중요한 변수라서 모든 곳에서 사용할 수 있게 하려면, 전역 객체에 직접 프로퍼티를 추가해서 사용한다.

- 전역 변수는 되도록 사용하지 않는 것이 좋다. 함수를 만들 때는 외부 변수나 전역 변수를 사용하는 것보다 '인풋'변수를 받고 이를 이용해 '아웃풋'을 만들어내개 해야 테스트도 쉽고 에러도 덜 만들어 낸다.

- 전역 객체를 이용해 현재 사용중인 프라우저가 최신 자바스크립트 기능을 지원하는지 여부를 확인할 수 있다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 6.5 전역 객체](https://ko.javascript.info/global-object)