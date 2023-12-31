## while and for

- loop statement를 사용하면 동일한 코드를 반복할 수 있다.

- **'while':** 'while(인수) { }'와 같이 선언하여 사용한다. condition이 인수로 전달되며 해당 condition이 truthy일 경우 중괄호 내부의 반복문 본문 코드가 실행된다. loop statement의 본문이 한 번 실행되는 것을 iteration이라고 한다. 반복문 조건에는 비교뿐만 아니라 모든 종류의 표현식과 변수가 선언될 수 있다. 조건은 while에 의해 평가되고, 평가 후엔 Boolean type 값으로 변경된다.

- **'do...while':** 'do...while' 문법을 사용하면 조건을 반복문의 본문 아래에 선언할 수 있다. 'do...while'의 경우 본문이 먼저 실행된 후 조건을 확인한다. 조건이 truthy인 동안에는 반복문의 본문을 계속 반복하여 실행한다. 'do...while' 문법은 조건에 상관 없이 본문을 최소 한 번 실행하고자 할 때 사용한다.

- **'for':** 'for(초기화 인수; 조건 인수; 반복 인수) { }'와 같이 선언하여 사용한다. 초기화 인수는 반복문에 진입할 때 단 한 번 실행된다. 조건 인수는 반복마다 조건을 확인하는데 사용하고 조건이 false이면 반복을 중지한다. 반복 인수는 각 iteration 이후 실행된다. 증괄호 내부에는 반복문 본문을 선언하고 조건의 평가값이 truthy일 동안에는 반복되어 실행된다. 각 인수들은 생략하고 선언할 수 있지만, 조건 인수를 생략하거나 따로 break 예약어를 선언하지 않을 경우 해당 반복문은 무한대로 반복 실행된다.

- **'break':** 'break' 예약어는 현재 코드 블록을 더 이상 실행하지 않고 빠져나갈 때 사용한다. 삼항연산자의 피연산자로 'break'를 사용하면 문법오류가 발생한다.

- **'continue':** 'continue' 예약어는 현재 코드 블록의 iteration을 멈추고 다음 iteration을 실행하기 위해 사용한다. 'for' 반복문의 경우 'continue'가 호출되면 조건을 평가한 후에 다음 iteration을 실행한다. 삼항연산자의 피연산자로 'continue'를 사용하면 문법오류가 발생한다.

- **label:** label을 'break' 예약어와 함께 사용할 경우 여러 개의 중첩 반복문을 한 번에 빠져나오도록 할 수 있다. 레이블은 '레이블 이름: for() { }'와 같이 선언하여 사용한다. 반복문 안에서 'break 레이블 이름;'와 같이 선언할 경우 해당 레이블로 지정된 반복문을 빠져나간다. 'continue' 예약어와 함께 label을 사용할 경우 레이블로 지정된 반복문의 다음 iteration이 실행된다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 2.13 while과 for 반복문](https://ko.javascript.info/while-for)