## new operator and constructor

- new 연산자와 constructor function(생성자 함수)를 사용하면 유사한 객체 여러 개를 쉽게 만들 수 있다.

- constructor function은 '함수 이름의 첫 글자를 대문자로 시작한다.', '반드시 new 연산자를 붙여 실행한다.'는 두 가지 관례를 따른다.

- 'new 생성자 함수 이름(인수)'로 생성자 함수를 실행하면 다음의 절차대로 실행된다. '빈 객체를 만들어 this에 할당한다. > 함수 본문을 실행하여 this에 새로운 프로퍼티를 추가하여 this를 수정한다. > this를 반환한다.'

- 재사용 할 수 있는 객체 생성 코드룰 구현하는 것에 생성자의 의의가 있다.

- 모든 함수는 생성자 함수가 될 수 있다. new 연산자를 붙여 실행하면 어떤 함수라도 위어 언급된 알고리즘이 실행된다. 이름의 첫 글자가 대문자인 함수는 new를 붙여 실행해야한다.

- new.target 프로퍼티를 사용하면 함수가 new와 함께 호출되었는지 아닌지를 알 수 있다. 함수를 일반적인 방법으로 호출했다면 new.target은 undefined를 반환한다. new와 함께 함수를 호출했다면 함수 자체를 반환한다. 함수 본문에서 new.target을 사용하면 해당 함수가 new와 함께 호출 되었는지 아닌지 확인할 수 있다. 이를 활용해 일반적인 방법으로 함수를 호출해도 new를 붙여 호출한 것과 같이 동작하도록 만들 수 있다. 이런 방식을 사용하면 new를 붙여 함수를 호출하든 아니든 코드가 동일하게 동작하기 때문에, 좀 더 유연하게 코드를 작성할 수 있다.

- constructor function은 반환해야 할 것들은 모두 this에 저장하고 this는 자동으로 반환되기 때문에 return을 명시적으로 쓸 필요가 없다.

- constructor function에서 객체를 리턴한다면 this 대신 객체가 반환된다. primitive type을 리턴하거나 아무것도 리턴하지 않을 경우에는 return문이 무시된다.

- 생성자 함수를 사용하면 매개변수를 이용해 객체 내부를 자유롭게 구성할 수 있다. this에 프로퍼티 뿐아니라 method를 더해주는 것도 가능하다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 4.5 new 연산자와 생성자 함수](https://ko.javascript.info/constructor-new)