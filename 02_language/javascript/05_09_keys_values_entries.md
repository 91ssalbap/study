## Object.keys, values, entries

- 일반 객체의 순회 관련 메서드는 'Object.keys(인수)', 'Object.values(인수)', 'Object.entries(인수)'와 같이 호출하며 인수에는 해당 객체가 전달된다.

- 일반 객체의 순회 관련 메서드는 iterable 객체를 반환하는 Map과 다르게 배열을 반환한다.

- Object.keys, values, entries는 심볼형 프로퍼티를 무시한다. 심볼형 키가 필요한 경우에는 'Object.getOwnPropertySymbols(인수)'를 사용하면 심볼형 키만 배열 형태로 반환한다. 'Reflect.ownKeys(인수)'를 사용하면 키 전체를 배열 형태로 반환한다.

- 'Object.entries(인수)'를 사용해 객체의 key-value 쌍이 요소인 배열을 얻는다. > 배열에 map 등의 배열 전용 메서드를 적용한다. > 배열 전용 메서드가 적용된 배열에 'Object.formEntries(인수)'를 적용해 배열을 객체로 되돌린다. 이러한 방법을 사용하면 객체에도 map, filter와 같은 배열 전용 메서드를 사용할 수 있다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 5.9 Object.keys, values, entries](https://ko.javascript.info/keys-values-entries)