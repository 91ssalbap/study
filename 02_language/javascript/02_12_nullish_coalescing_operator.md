## nullish coalescing operator

- nullish coalescing operator(nullish 병합 연산자) '??'를 사용하면 짧은 문법으로 여러 피연산자 중 그 값이 '확정되어있는' 변수를 찾을 수 있다.

- 'a ?? b'의 경우 a가 null 또는 undefined가 아니면 a의 값을 반환하고 a가 null 또는 undefined일 경우 b의 값을 반환한다. nullish coalescing operator을 사용하지 않으면 '(a !== null && a !== undefined) ? a : b;'처럼 코드가 길어진다. 

- '??'는 왼쪽의 피연산자부터 평가하여 null이나 undefined가 아닌 첫 번째 피연산자의 값을 반환한다. 'null ?? undefined ?? "a" ?? "b"'의 경우 "a"가 반환된다.

- '||'는 첫 번째 truthy 값을 반환한다. '??'는 첫 번째 defined(정의된) 값을 반환한다. '0 || 100, 0 ?? 100'에서 왼쪽 연산은 100을 반환하고 오른쪽 연산은 0을 반환한다 '||'는 0을 falsy한 값으로 취급하기 때문이고 '??'는 0을 defined 값으로 평가하기 때문이다. 0이 할당될 수 있는 변수를 피연산할 때는 '||'보다 '??'이 적합하다.

- '??'의 연산자 우선순위는 낮은편이다. 괄호를 추가해 연산하는걸 권장한다.

- '??' 는 '||'나 '&&'와 함께 사용하지 못한다. 안정성 관련 이슈로 함께 사용하면 문법 에러가 발생한다. 괄호를 사용하면 제약을 피할 수 있다.

### 참조
---

- [모던 JavaScript 튜토리얼 - 2.12 nullish 병합 연산자 '??'](https://ko.javascript.info/nullish-coalescing-operator)