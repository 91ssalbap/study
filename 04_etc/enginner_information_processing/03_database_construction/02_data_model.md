## data model

### 데이터 모델의 구성요소

1. 개체(Entity)
  - 데이터베이스에 표현하려는 것이다.
  - 사람이 생각하는 개념이나 정보 단위 같은 현실 세계의 대상체를 의미한다.

2. 속성(Attribute)
  - 데이터의 가장 작은 논리적 단위이다.
  - 파일 구조상의 데이터 항목 또는 데이터 필드에 해당한다.

3. 관계(Relationship)
  - 개체 간의 관계 또는 속성 간의 논리적 연결을 의미한다.

### 개념적 데이터 모델

+ 현실 세계에 대한 인간의 이해를 돕기 위해 현실 세계에 대한 인식을 추상적 개념으로 표현하는 과정을 말한다.

+ 주로 E-R(Entity-Relation)모델을 사용한다.

### 논리적 데이터 모델

+ 개념적 모델링 과정에서 얻은 개념적 구조를 컴퓨터가 이해햐고 처리할 수 있는 컴퓨터 세계의 환경에 맞도록 변환하는 과정을 말한다.

+ 단순히 데이터 모델이라고 하면 논리적 데이터 모델을 의미한다.

+ 관계 모델, 계층 모델, 네트워크 모델이 있다.

### 데이터 모델에 표시할 요소

1. 구조(Structure)
  - 논리적인 개체 타입들 간의 관계를 말한다.
  - 데이터 구조 및 정적 성질을 표현한다.

2. 연산(Operation)
  - 실제 데이터를 처리하는 작업에 대한 명세이다.
  - 조작하는 기본 도구이다.

3. 제약 조건(Constraint)
  - DB에 저장될 수 있는 실제 데이터의 논리적인 제약 조건을 말한다.