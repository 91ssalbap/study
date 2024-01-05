## if statement and conditional operator

### if statement
---

- 'if(인수)'는 인수로 전달되는 조건을 평가하여 조건이 true이면 코드 블록을 실행한다. 코드 블록은 중괄호로 감싸는것이 권장된다.

- 'if(인수)'는 인수로 전달되는 조건을 평가하고 결과를 Boolean type으로 변환한다. 평가 결과가 숫자 0, 빈 문자열, null, undefined, NaN과 같은 falsy(거짓 같은) 값들일 경우 false로 변환된다. truthy(참 같은) 값들은 true로 변환된다.

- 'else'는 if statement 뒤에 선언하여 사용한다. else의 코드 블록은 'if(인수)'가 false를 반환할 경우 실행된다.

- 'else if(인수)'는 조건 여러 개를 처리해야할 경우 if statement 뒤에 선언해서 사용한다. 'if(인수)'가 false를 반환할 경우 그 뒤에 선언되어있는 'else if(인수)'를 평가하여 true면 실행하고 false면 실행하지 않는다. 'else if(인수)' 뒤에는 다른 'else if(인수)'나 'else'를 선언하거나 아무것도 선언하지 않고 다음 statement로 넘어갈 수 있다.

### conditional operation '?'

- 조건에 따라 다른 값을 변수에 할당할 때 사용한다. if statement를 사용하는 것보다 더 짧고 간결하게 조건의 true, false 여부에 따라 다른 값을 반환 할 수 있다. conditional operation은 '?'로 표시하며 피연산자가 세 개이기 때문에 ternary(삼항) operation이라고 부르기도 한다. '평가 대상 ? 평가가 true일 경우 반환되는 값 : 평가가 false일 경우 반환되는 값'의 형식으로 사용된다.

- conditional operation은 다중으로 선언하여 복수의 조건을 처리할 수 도 있다.

- conditional operation의 반환 값에는 statement를 선언하여 사용하는 것을 지양한다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 2.10 if와 '?'를 사용한 조건 처리](https://ko.javascript.info/ifelse)