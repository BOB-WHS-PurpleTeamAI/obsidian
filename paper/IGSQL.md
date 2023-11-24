[[paper]]
IGSQL: Database Schema Interaction Graph Based Neural Model for Context-Dependent Text-to-SQL Generation

([https://paperswithcode.com/paper/igsql-database-schema-interaction-graph-based](https://paperswithcode.com/paper/igsql-database-schema-interaction-graph-based))

- **동기**: 컨텍스트 의존적인 Text-To-SQL 생성은 사용자가 자연어로 데이터베이스에 질의할 수 있게 하는 작업이다. 이 작업은 대화 시나리오에서 이전의 사용자 입력과 데이터베이스 스키마 항목을 고려해야 한다.
- **모델 설계**: IGSQL 모델은 Encoder-Decoder 프레임워크를 사용한다. 인코더는 텍스트 인코더와 데이터베이스 스키마 인터랙션 그래프 인코더로 구성된다. 텍스트 인코더는 BERT 임베딩과 LSTM을 사용하여 이전의 사용자 입력을 인코딩한다. 데이터베이스 스키마 인터랙션 그래프 인코더는 데이터베이스 스키마 항목을 노드로 하는 그래프를 구축하고, 이전의 스키마 항목과 현재의 스키마 항목 사이의 관계를 모델링한다. 디코더는 LSTM과 어텐션 메커니즘을 사용하여 SQL 토큰을 생성한다. 또한, 게이트 메커니즘을 도입하여 SQL 예약어, 데이터베이스 스키마 항목, 이전에 생성된 SQL 토큰 중에서 중요한 단어를 가중치를 부여한다.
- **결과**: SParC와 CoSQL이라는 두 개의 크로스 도메인 컨텍스트 의존적인 Text-To-SQL 데이터셋에서 실험을 수행하였다. IGSQL 모델은 이전의 최고 성능 모델인 EditSQL보다 질문 정확도와 상호작용 정확도에서 모두 큰 폭으로 개선하였다. IGSQL 모델은 데이터베이스 스키마 항목의 역사적 정보를 활용하여 대화 시나리오에서 문맥 일관성을 유지하는 데 효과적임을 보여주었다.