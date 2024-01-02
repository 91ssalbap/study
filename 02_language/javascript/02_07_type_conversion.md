## type conversion

- 함수와 연산자에 전달되는 값은 대부분 적절한 자료형으로 자동 변환된다. 이를 type conversion(형 변환)이라고 한다.

- 전달 받은 값을 의도적으로 원하는 타입으로 변환(명시적 변환)하는 경우도 형 변환이라고 한다.

### conversion to string type
---

- alert()과 같이 문자열만 사용하는 함수/연산자에서는 다른 자료형의 인자를 전달하더라도 문자형으로 자동 변환 된다.

- String(인자) 함수를 호출해 다른 자료형의 인자를 명시적으로 형변환 할 수 있다.

- 예를 들어 false, null은 각각 "false"와 "null"로 변환된다.

### conversion to number type
---

- 수학과 관련된 함수와 표현식에서는 다른 자료형들이 숫자형으로 자동 형변환된다.

- Number(인자) 함수를 사용해서 다른 자료형의 인자를 명시적으로 형변환 할 수 있다.

- 숫자 이외의 글자가 들어있는 문자열을 숫자형으로 변환하려고 할 경우 그 결과로 NaN이 도출된다. 

- undefined, null, true, false는 각각 NaN, 0, 1, 0으로 변환된다.

- 문자열은 처음과 끝의 공백이 제거되고 남아있는 문자열이 없다면 0, 문자열에 숫자만 있다면 해당 숫자를 숫자형으로 변환, 글자가 있어서 변환에 실패하면 NaN이 된다.

### conversion to boolean type
---

- Boolean(인자)를 호출하면 다른 자료형의 인자를 명시적으로 형변환 할 수 있다.

- 0, ""(빈 문자열), null, undefined, NaN은 false로 변환된다. 이외의 값들은 true로 변환된다. "0"(문자열 0)은 true로 변환된다.


### 참조
---

- [모던 JavaScript 튜토리얼 - 2.7 형 변환](https://ko.javascript.info/type-conversions)