## nullish coalescing operator

- nullish coalescing operator(nullish 병합 연산자) '??'를 사용하면 짧은 문법으로 여러 피연산자 중 그 값이 '확정되어있는' 변수를 찾을 수 있다.

- 'a ?? b'의 경우 a가 null 또는 undefined가 아니면 a의 값을 반환하고 a가 null 또는 undefined일 경우 b의 값을 반환한다. nullish coalescing operator을 사용하지 않으면 '(a !== null && a !== undefined) ? a : b;'처럼 코드가 길어진다. 

- '??'는 왼쪽의 피연산자부터 평가하여 null이나 undefined가 아닌 첫 번째 피연산자의 값을 반환한다. 'null ?? undefined ?? "a" ?? "b"'의 경우 "a"가 반환된다.

- '||'는 첫 번째 truthy 값을 반환한다. '??'는 첫 번째 defined(정의된) 값을 반환한다.