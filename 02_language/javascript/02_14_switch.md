## switch

- switch statement는 특정 변수를 다양한 상황에서 비교할 수 있게 한다. 코드에서 비교 상황을 잘 설명한다. 복수의 if condition statement를 대체할 수 있다.

- 복수의 case statement로 구성된다. default statement도 있지만 필수는 아니다.

- 변수와 case statement의 값이 일치하면 해당 case statement를 실행한다. break 예약어가 없을 경우 이어지는 case statement 또는 default statement를 평가 없이 실행한다.

- 변수와 case statement의 값이 일치하지 않을 경우 이어지는 case statement의 값을 평가한다. 마지막 case statement의 값까지 일치하지 않을 경우 switch statement를 종료하거나 default statement가 있을 경우 default statement만 실행한다.

- switch와 case statement은 모든 형태의 표현식을 인수로 받는다.

- break 예약어가 없는 경우 조건에 상관없이 다음 case statement가 실행된다는 점을 이용해서 복수의 case문을 묶어 선언할 수 있다.

- switch의 인수와 case의 인수는 data type까지 같아야 일치한 것으로 평가된다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 2.14 switch문](https://ko.javascript.info/switch)