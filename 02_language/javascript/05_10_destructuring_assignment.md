## destructuring assignment

- destructuring assignment(구조 분해 할당)를 사용하면 객체나 배열을 변수로 분해하여 함수에 객체나 배열의 전체 또는 일부를 전달할 수 있다. 매개변수가 많거나 매개변수 기본값이 필요한 경우에도 destructuring assignment를 사용할 수 있다.
```javascript
    // 값 "value1", "value2"를 요소로 가진 배열
    let array1 = ["value1", "value2"];

    // 구조 분해 할당을 이용해
    // value1 변수에는 값 "value1"을 할당
    // value2 변수에는 값 "value2"를 할당
    let [value1, value2] = array1;

    alert(value1);  // value1
    alert(value2);  // value2
```

- 'split()'과 같은 반환 값이 배열인 매서드와 함께 사용할 수 있다.
```javascript
    let [value1, value2] = "value1 value2".split(' ');

    alert(value1);  // value1
    alert(value2);  // value2
```

- 구조 분해 할당 과정에서 분해 대상이 수정되거나 파괴되는것은 아니다.

- 쉼표를 사용하면 필요하지 않은 배열 요소를 버릴 수 있다.
```javascript
    // 배열의 요소 중 필요하지 않은 "value2"는 제외하고 할당한다.
    let[value1, , value3] = ["value1", "value2", "value3"];

    alert(value1);  // value1
    alert(value3);  // value3
```

- 할당 연산자 우측에는 모든 itreable 객체를 선언할 수 있다.

- 할당 연산자 좌측에는 assignables(할당할 수 있는)한 것이라면 무엇이든 선언할 수 있다. 객체 프로퍼티도 선언할 수 있다.

- 'Object.entries(인수)'와 destructing assignment를 조합하면 객체 또는 맵의 키와 값을 순회해 변수로 분해 할당 할 수 있다.
```javascript
    let object1 = {
        key1: "value1",
        key2: "value2"
    };

    for (let [key, value] of Object.entries(object1)) {
        alert(`${key} : ${value}`); // key1 : value1, key2 : value2가 차례대로 출력된다.
    }

    let map1 = new Map();
    map1.set("key1", "value1");
    map1.set("key2", "value2");

    for (let [key, value] of map1) {
        alert(`${key} : ${value}`); // key1 : value1, key2 : value2가 차례대로 출력된다.
    }
```

- 두 변수에 저장된 값을 교환할 때 구조 분해 할당을 사용할 수 있다.
```javascript
    let value1 = "value1";
    let value2 = "value2";

    // 변수 value1에 value2의 값을, 변수 value2에 value1의 값을 교환하여 할당한다.
    [value1, value2] = [value2, value1];

    alert(value1);  // value2
    alert(value2);  // value1
```

- '...'를 붙인 매개변수를 사용하면 이미 호출한 배열 앞쪽 값 몇 개를 재외하고 나머지 값들은 한번에 호출하여 처리할 수 있다. '...'을 붙인 매개변수는 마지막에만 사용할 수 있다.
```javascript
    let [value1, value2, ...valueN] = ["value1", "value2, "value3", "value4"];

    alert(value1);          // value1
    alert(value2);          // value2
    alert(valueN[0]);       // value3
    alert(valueN[1]);       // value4
    alert(valueN.length)    // 2
```  