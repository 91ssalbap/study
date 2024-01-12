## map and set

- Map은 키가 있는 데이터를 저장한다는 점에서 객체와 유사하다. Map은 키에 다양한 자료형을 허용한다는 점에서 차이가 있다. 객체는 key를 문자형으로 변환하지만 Map은 키의 원래 타입을 그대로 유지한다. 객체 타입도 key로 사용할 수 있다.

- 'new Map()'으로 맵을 생성한다. 'map.set(인수, 인수)'으로 첫 번째 인수 key를 이용해 두 번째 인수 value를 저장한다. 'map.get(인수)' 인수에 key를 전달하여 그에 해당하는 value를 호출한다. key가 존재하지 않을 경우 undefined가 반환된다. 'map.has(인수)' 인수에 전달한 key가 Map에 존재하면 true, 존재하지 않으면 false를 반환한다. 'map.delete(인수)' 인수로 전달된 key에 해당하는 value를 삭제한다. 'map.clear()' Map안의 모든 요소를 제거한다. 'map.size' Map이 가지고 있는 요소의 개수를 반환한다.

- Map에 요소를 할당할 때 'map\[key\] = value'의 방식은 권장되지 않는다. 전용 메서드 set, get등을 사용하는 것을 권장한다.

- Map은 SameValueZero 알고리즘을 사용해 값의 등가 여부를 확인한다. static equality operator와 유사하지만 NaN과 NaN을 같아고 취급하는 것에서 일치 연산자와 차이가 있다.

- 'map.set()'을 호출할 때마다 Map 자신이 반환된다. 이를 이용하여 'map.set()'을 chaining(체이닝) 할 수 있다.