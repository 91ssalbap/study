# weak map and weak set

- 자료구조를 구성하는 요소는 자신이 속한 자료구조가 메모리에 남아있는 동안 대개 도달 가능한 값으로 취급되어 메모리에서 삭제되지 않는다. 객체의 프로퍼티나 배열의 요소, 맵이나 셋을 구성하는 요소들이 이에 해당한다.

- WeakMap(위크맵)을 사용하면 키로 쓰인 객체가 가비지 컬렉션의 대상이 된다.

- WeakMap의 키는 반드시 객체여야 한다. 원시값은 WeakMap의 key가 될 수 없다.

- WeakMap의 키로 사용된 객체를 참조하는 것이 아무것도 없다면 해당 객체는 메모리와 위크맵에서 자동으로 삭제된다.

- WeakMap은 반복 작업과 keys(), values(), entries() 메서드를 지원하지 않는다. 'weakMap.get(인수)', 'weakMap.set(인수, 인수)', 'weakMap.delete(인수)', 'weak.has(인수)'만 지원한다. 적은 메서드만 지원하는 이유는 가비지 컬렉션의 동작 시점을 정확히 알 수 없어서 현재 WeakMap에 요소가 몇 개나 있는지 정확히 파악할 수 없기 때문이다.

- WeakMap은 부차적인 데이터를 저장할 곳이 필요할 때 사용한다. WeakMap의 value는 해당 value의 key인 object가 메모리에서 지워지면 자동으로 함께 지워진다.

- WeakSet은 객체만 저장할 수 있다. 원시값은 저장할 수 없다.

- WeakSet 안의 객체는 도달 가능할 때만 메모리에서 유지된다.

- WeakSet은 'weakSet.add(인수)', 'weakSet.has(인수)', 'weakSet.delete(인수)'를 사용할 수 있다. size, keys()나 반복 관련 메서드는 사용할 수 없다.

- WeakSet은 부차적인 데이터를 저장할 때 사용한다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 5.8 위크맵과 위크셋](https://ko.javascript.info/weakmap-weakset)