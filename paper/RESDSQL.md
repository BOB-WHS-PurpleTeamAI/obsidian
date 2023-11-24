[[paper]]
RESDSQL: Decoupling Schema Linking and Skeleton Parsing for Text-to-SQL

([https://paperswithcode.com/paper/decoupling-the-skeleton-parsing-and-schema](https://paperswithcode.com/paper/decoupling-the-skeleton-parsing-and-schema))

- **문제 정의**: Text-To-SQL 생성은 사용자가 자연어로 데이터베이스에 질의할 수 있게 하는 작업이다. 이 작업은 스키마 링킹과 스켈레톤 파싱이라는 두 가지 하위 작업을 포함한다. 스키마 링킹은 질문에서 언급된 개체를 데이터베이스 스키마 항목과 연결하는 작업이고, 스켈레톤 파싱은 질문의 의미를 반영하는 SQL 쿼리의 뼈대를 구성하는 작업이다. 이 두 가지 작업은 서로 얽혀 있어서 Text-To-SQL 생성의 난이도를 높인다.
- **모델 설계**: RESDSQL 모델은 Encoder-Decoder 프레임워크를 사용한다. Encoder는 텍스트 인코더와 스키마 링킹 인코더로 구성된다. 텍스트 인코더는 T5와 같은 사전학습된 언어 모델을 사용하여 질문을 인코딩한다. 스키마 링킹 인코더는 크로스-인코더를 사용하여 각 스키마 항목에 대한 확률을 계산하고, 확률에 따라 스키마 항목을 순위별로 정렬하고 필터링하여 순위화된 스키마 시퀀스를 생성한다. Decoder는 T5와 같은 사전학습된 언어 모델을 사용하여 SQL 쿼리를 생성한다. 또한, SQL 쿼리 생성을 두 단계로 분리하여, 먼저 SQL 쿼리의 스켈레톤을 생성하고, 그 다음에 스켈레톤에 필요한 데이터를 채워넣는다.
- **결과**: Spider와 그 변형 버전인 Spider-DK, Spider-Syn, Spider-Realistic이라는 네 개의 Text-To-SQL 데이터셋에서 실험을 수행하였다. RESDSQL 모델은 기존의 최고 성능 모델들보다 EM과 EX라는 두 가지 평가 지표에서 모두 우수한 성능을 보였다. RESDSQL 모델은 스키마 링킹과 스켈레톤 파싱을 분리함으로써 Text-To-SQL 생성의 난이도를 줄이고, 질문 변형에 대한 강건성을 향상시킴을 보여주었다.