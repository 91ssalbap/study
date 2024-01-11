## iterable object

- iterable(반복 가능한) 객체는 배열을 일반화한 객체이다. 이터러블이라는 개념을 사용하면 어떤 객체에는 for..of 반복문을 적용할 수 있다. 배열, 문자열 등이 대표적인 이터러블 객체에 해당한다.

- 배열이 아니지만 어떤 것들의 컬렉션(목록, 집합 등)을 나타내고 있는 경우에 for...of 문법을 적용할 수 있다면 해당 컬렉션을 순회하는데 유용하다.

- 객체를 iterable로 만들려면 객체에 Symbol.iterator(특수 내장 심볼)라는 메서드를 추가해야 한다. Symbol.iterator를 추가하면 for...of는 Symbol.iterator를 호출한다. Symbol.iterator 메서드는 메서드 next()가 있는 객체 이터레이터를 반환해야한다. 이후 for...of는 반환된 이터레이터 객체만을 대상으로 동작한다. for...of에 다음 값이 필요하면 for...of는 이터레이터 객체의 next() 메서드를 호출한다. 메서드 next()의 반환값은 '{done: Boolean, value: any}'와 같은 형태여야 한다. done의 값이 true일 땐 다음 값이 없어 반복이 종료됨을 의미한다. done의 값이 false일 땐 다음 값이 존재하므로 반복이 계속 진행되고 value에 다음 값이 할당된다.