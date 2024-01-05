## basic operator and math operator

- **operand(피연산자):** 연산자가 연산을 수행하는 대상이다. argument(인수)라고 불리기도 한다.

- **unary operators(단항 연산자):** 피연산자를 하나만 받는 연산자이다.

- **binary operators(이항 연산자):** 두 개의 피연산자를 받는 연산자이다.

### math operator(수학 연산자)
---

- 자바스크립트에서 제공하는 수학 연산자에는 '+', '-', '*', '/', '%', '**'가 있다.

- **remainder operator(%, 나머지 연산자):** 좌항의 피연산자를 우항의 피연산자로 나눈 후 그 나머지를 정수로 반환한다.

- **expornentiation operator(\*\*, 거듭제곱 연산자):** 좌항의 피연산자를 우항의 피연산자 만큼 곱한 값이 반환된다. 우항에는 정수가 이닌 숫자도 선언할 수 있다. '1/2'와 같은 숫자를 거듭제곱하는 것으로 제곱근을 구할 수도 있다.

### javascript operator(자바스크립트 연산자)
---

- **binary operator '+' with String type:** 문자열이 '+' 연산자의 피연산자일때 '+' 연산자는 덧셈을 수행하지 않고 문자열을 병합한다. 이항 연산자 '+'의 피연산자 중 하나라도 String type일 경우 나머지 하나도 String type으로 type conversion(형변환)된다. 다른 산술 연산자들이 피연산자가 숫자형이 아닌 경우에 그 형을 숫자형으로 형변환 하는 것과 대조적이다.

- **unary operator '+' with conversion to number type:** 숫자형이 아닌 피연산자에 단항 '+'연산자를 붙이면 해당 피연산자를 숫자형으로 변환한다. 'Number(인수)'와 동일한 일을 수행한다. 문자형 숫자 피연산자들을 '+' 연산하여 숫자형 피연산자들을 '+'연산한 것과 동일한 결과를 얻고자 할때 각 피연산자에 '+' 단항 연산자를 붙여서 연산하면 원하는 결과를 얻을 수 있다.

- **assignment operator '=':** 무언가를 할당할 때 쓰이는 연산자이다. 값을 할당할 뿐만 아니라 반환한다. 표현식에서 다른 연산자의 피연산자로 사용할 수 있지만 지양한다. 할당 연산자를 여러개 연결해 사용하는 것을 할당 연산자 체이닝이라고 한다. 변수에 연산자를 적용하고 그 결과를 같은 변수에 저장해야 하는 경우 복합 할당 연산자를 사용한다. 변수의 숫자를 하나 늘리거나 줄이고자 할 때는 증가, 감소 연산자를 사용할 수 있다. 전위형 증가, 감소 연산자는 변수의 숫자를 증가,감소시킨 후 표현식을 연산한다. 후위형 증가, 감소 연산자는 표현식을 연산 한 후에 변수의 숫자를 증가,감소시킨다.

- **bitwise operator:** 인수를 32비트 정수로 변환하여 이진 연산을 수행한다. AND(&), OR(|), XOR(^), NOT(~), 왼쪽 시프트(<<), 오른쪽 시프트(>>), 부호 없는 오른쪽 시프트(>>>)가 있다. 암호를 다룰때 유용하게 사용된다.

- **comma operator ',':** 여러 표현식을 코드 한줄에서 평가할 수 있게 한다. 표현식 각각이 모두 평가 되지만, 마지막 표현식의 평가 결과만 한환된다.

### 연산자 우선 순위
---

- 하나의 표현식에 둘 이상의 연산자가 있는 경우 연산자 우선 순위에 의해 실행 순서가 결정된다.

- 괄호는 모든 연산자보다 우선순위가 높다.

- 우선순위 숫자가 클수록 먼저 실행된다. 같으면 왼쪽부터 시작해서 오른쪽으로 연산이 수행된다.

- 동일한 기호의 단항 연산자는 이항 연산자보다 우선순위가 더 높다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 2.8 기본 연산자와 수학](https://ko.javascript.info/operators)