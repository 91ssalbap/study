## map and set

- Map은 키가 있는 데이터를 저장한다는 점에서 객체와 유사하다. Map은 키에 다양한 자료형을 허용한다는 점에서 차이가 있다. 객체는 key를 문자형으로 변환하지만 Map은 키의 원래 타입을 그대로 유지한다. 객체 타입도 key로 사용할 수 있다.

- 'new Map()'으로 맵을 생성한다. 'map.set(인수, 인수)'으로 첫 번째 인수 key를 이용해 두 번째 인수 value를 저장한다. 'map.get(인수)' 인수에 key를 전달하여 그에 해당하는 value를 호출한다. key가 존재하지 않을 경우 undefined가 반환된다. 'map.has(인수)' 인수에 전달한 key가 Map에 존재하면 true, 존재하지 않으면 false를 반환한다. 'map.delete(인수)' 인수로 전달된 key에 해당하는 value를 삭제한다. 'map.clear()' Map안의 모든 요소를 제거한다. 'map.size' Map이 가지고 있는 요소의 개수를 반환한다.

- Map에 요소를 할당할 때 'map\[key\] = value'의 방식은 권장되지 않는다. 전용 메서드 set, get등을 사용하는 것을 권장한다.

- Map은 SameValueZero 알고리즘을 사용해 값의 등가 여부를 확인한다. static equality operator와 유사하지만 NaN과 NaN을 같아고 취급하는 것에서 일치 연산자와 차이가 있다.

- 'map.set()'을 호출할 때마다 Map 자신이 반환된다. 이를 이용하여 'map.set()'을 chaining(체이닝) 할 수 있다.

- 'map.key()'는 각 요소의 키를 모은 iterable object를 반환한다. 'map.values()'는 각 요소의 값을 모은 iterable 객체를 반환한다. 'map.entries()'는 각 요소의 key, value를 한 쌍으로 하는 iterable 객체를 반환한다.

- map은 삽입 순서를 기억하므로 값이 삽입된 순서대로 순회한다. 객체라 프로퍼티의 순서를 기억하지 못하는 것과 차이를 보인다.

- map에는 for...of, forEach 반복문을 사용할 수 있다.

- 각 요소가 key-value 쌍인 배열이나 이터러블 객체를 초기화 용도로 Map에 전달해 새로운 Map을 만들 수 있다. Object.entries(인수)를 활용하면 인수에 전달된 평범한 객체의 key-value 쌍을 요소로 가지는 배열을 반환한다. 평범한 객체를 가지고 Map을 만들 수 있다.

- Object.fromEntries(인수)를 사용해서 인수에 key-value 쌍인 배열을 전달하면 객체를 생성해 반환한다. map.entries()를 사용해 Map의 각 요소의 key-value를 한 쌍으로 하는 iterable 객체를 얻는다. 해당 iterable 객체를 Object.formEntries(인수)의 인수로 전달하면 map을 사용해 객체를 생성할 수 있다. map.entries()를 호출하지 않고 Object.fromEntries(인수)의 인수로 map을 바로 전달해도 같은 값을 반환 받을 수 있다.

- Set은 중복을 허용하지 않는 값을 모아놓은 Collection이다. key가 없는 값이 저장된다.

- 'new Set(인수)'로 Set을 생성한다. 인수에 iterable 객체를 전달하면 해당 iterable 객체의 값을 복사해 Set에 할당한다. 'set.add(인수)'로 Set에 인수로 전달한 값을 추가하고 해당 Set을 반환한다. 'set.delete(인수)'로 인수에 전달 값을 제거한다. 제거에 성공하면 true, 실패하면 false를 반환한다. 'set.has(인수)'로 인수에 전달 받은 값이 Set 내부에 존재하는지 확인한다. 값이 존재하면 true, 존재하지 않으면 false를 반환한다. 'set.clear()'로 Set을 비운다. 'set.size'로 Set에 있는 값의 개수를 확인한다.

- for...of나 forEach를 사용하면 Set의 값을 대상으로 반복 작업을 수행할 수 있다. set의 forEach에 사용하는 콜백함수에는 세 개의 인수를 받는다. 이 중 첫 번째와 두 번째는 같은 값이 전달된다. 이는 맵과의 호환성 때문이다. 이상하지만 이로인해 맵을 셋으로 셋을 맵으로 교체하기가 쉽다.

- 'set.keys()'는 Set 내의 모든 값을 포함하는 iterable 객체를 반환한다. 'set.values()'는 'set.keys()'와 동일한 작업을 수행한다. Map과의 호환성을 위해 만들어진 메서드이다. 'set.entries()'는 Set 내의 각 값을 이용해 만든 \[value, value\] 배열을 포함하는 iterable 객체를 반환한다. Map과의 호환성을 위해 만들어졌다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 5.7 맵과 셋](https://ko.javascript.info/map-set)