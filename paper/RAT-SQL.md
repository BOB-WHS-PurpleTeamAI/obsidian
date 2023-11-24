[[paper]]
RAT-SQL: Relation-Aware Schema Encoding and Linking for Text-to-SQL Parsers

([https://paperswithcode.com/paper/rat-sql-relation-aware-schema-encoding-and-1](https://paperswithcode.com/paper/rat-sql-relation-aware-schema-encoding-and-1))

- **동기**: 이 논문은 데이터베이스에서 질문에 답할 수 있는 SQL 쿼리로 자연어 질문을 번역하는 문제를 다룬다. 주요 도전 과제는 데이터베이스 스키마를 의미 분석 파서가 접근할 수 있는 방식으로 인코딩하고, 질문에서 열과 테이블을 참조하는 부분을 스키마 엔티티와 연결하는 것이다.
- **방법**: 이 논문은 RAT-SQL이라는 통합 프레임워크를 제안한다. 이 프레임워크는 관계 인식 셀프 어텐션(relation-aware self-attention)을 사용하여 질문 단어와 스키마 요소 사이의 미리 정의된 관계와 유도된 관계를 모두 인코딩한다. 이 프레임워크는 스키마 인코더, 스키마 링커, 트리 구조 디코더로 구성된다. 스키마 인코더는 그래프 신경망(graph neural network)을 사용하여 스키마 구조를 인코딩하고, 관계 인식 트랜스포머(relation-aware transformer)를 사용하여 질문과 맥락화한다. 스키마 링커는 이름 기반과 값 기반의 방법을 사용하여 질문 단어와 스키마 열과 테이블을 정렬한다. 디코더는 인코딩된 표현에 대한 포인터 메커니즘을 사용하여 SQL 쿼리를 추상 구문 트리(abstract syntax tree)로 생성한다.
- **결과**: 이 논문은 RAT-SQL을 Spider 데이터셋에 적용하여 복잡한 Text-To-SQL 작업에 대해 평가합니다. Spider 데이터셋은 학습하지 않은 데이터베이스 스키마에 대한 일반화가 필요한 데이터셋이다. RAT-SQL은 테스트 세트에서 57.2%의 정확도를 달성하여, 최고의 대안 모델보다 8.7%의 절대적인 개선을 보인다. BERT와 결합하면 Spider 리더보드에서 새로운 최고 성능인 65.6%를 달성했다. 또한, 이 논문은 모델이 스키마 링킹과 정렬에 대한 이해력을 개선하는 것을 정성적으로 보여준다.