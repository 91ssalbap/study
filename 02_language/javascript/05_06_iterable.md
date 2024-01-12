## iterable object

- iterable(반복 가능한) 객체는 배열을 일반화한 객체이다. 이터러블이라는 개념을 사용하면 어떤 객체에는 for..of 반복문을 적용할 수 있다. 배열, 문자열 등이 대표적인 이터러블 객체에 해당한다.

- 배열이 아니지만 어떤 것들의 컬렉션(목록, 집합 등)을 나타내고 있는 경우에 for...of 문법을 적용할 수 있다면 해당 컬렉션을 순회하는데 유용하다.

- 객체를 iterable로 만들려면 객체에 Symbol.iterator(특수 내장 심볼)라는 메서드를 추가해야 한다. Symbol.iterator를 추가하면 for...of는 Symbol.iterator를 호출한다. Symbol.iterator 메서드는 메서드 next()가 있는 객체 이터레이터를 반환해야한다. 이후 for...of는 반환된 이터레이터 객체만을 대상으로 동작한다. for...of에 다음 값이 필요하면 for...of는 이터레이터 객체의 next() 메서드를 호출한다. 메서드 next()의 반환값은 '{done: Boolean, value: any}'와 같은 형태여야 한다. done의 값이 true일 땐 다음 값이 없어 반복이 종료됨을 의미한다. done의 값이 false일 땐 다음 값이 존재하므로 반복이 계속 진행되고 value에 다음 값이 할당된다.

- iterable object의 핵심은 Seperation of Concern(SoC, 관심사의 분리)에 있다. iterable object에는 next() 메서드가 없다. 대신 '함수명\[Symbol.iterator\]()'를 호출해서 만든 이터레이터 객체와 이터레이터 객체의 메서드 next()에서 반복에 사용될 값을 만들어낸다. 이를 통해 iterator object와 iterable object를 분리할 수 있다. 두 객체를 합쳐서 iterable object 자체를 iterator object로 만들면 코드는 더 간단해진다. 이때에는 Symbol.iterator()가 iterable object 자체를 반환한다. iterable object 자체를 iterator object로 만들면 두 개의 for...of 반복문을 하나의 객체에 동시에 사용할 수 없다는 단점이 있다. iterator object가 하나뿐이라 두 반복문이 반복 상태를 공유하기 때문이다.

- 문자열은 iterable 객체다. for...of는 문자열의 각 글자를 순회한다. surrogate pair에도 잘 동작한다.

- iterator 객체를 명시적으로 호출할 경우 for...of를 사용하는 것 보다 반복과정을 더 잘 통제할 수 있다. 반복을 시작했다가 잠시 멈춰 다른 작업을 하다가 다시 반복을 시작하는 것 같이 반복 과정을 여러개로 쪼개는 것이 가능하다.

-  iterable과 array-like(유사 배열)는 비슷해 보이지만 아주 다른 개념이다. iterable 객체는 Symbol.iterator()가 구현되어있는 객체를 의미한다. array-like는 index와 length property가 있어서 배열처럼 보이는 객체이다. 문자열은 iterable 객체이면서 array-like이다. iterable과 유사 배열은 배열이 아니므로 push, pop 등의 메서드를 지원하지 않는다.

- 'Array.from(인수)' 메서드는 iterable 객체나 array-like를 인수로 받아 배열을 반환한다. 'Array.from()'의 두 번째 인수로 mapping 함수를 선택적으로 전달할 수 있다. mapping 함수를 전달하면 첫 번째 인수의 각 요소를 새로운 배열에 할당하기 전에 각 요소를 대상으로 mapping 함수를 실행하여 반환된 값을 새로운 배열에 항단한다. 'Array.form()'의 세 번째 인수에는 각 요소의 this로 지정할 값을 전달해 사용할 수 있다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 5.6 iterable 객체](https://ko.javascript.info/iterable)