[[paper]]
Graphix-T5: Mixing Pre-Trained Transformers with Graph-Aware Layers for Text-to-SQL Parsing

([https://paperswithcode.com/paper/graphix-t5-mixing-pre-trained-transformers](https://paperswithcode.com/paper/graphix-t5-mixing-pre-trained-transformers))

- **목적**: 자연어 질문을 실행 가능한 SQL 쿼리로 변환하는 Text-To-SQL 파싱 작업에서 도메인 일반화를 향상시키기 위해, 사전 훈련된 Test-To-Text 변환기 모델인 T5에 그래프 기반의 구조적 정보를 결합하는 새로운 아키텍처를 제안함.
- **방법**: GRAPHIX-T5라는 모델은 T5의 인코더를 그래프 인식 레이어로 대체하여, 질문과 데이터베이스 스키마 간의 명시적이고 암시적인 관계를 그래프로 표현하고, 그래프 신경망을 통해 다중 홉 추론을 수행한다. 또한, T5의 사전 훈련된 맥락 인코딩 능력을 유지하기 위해, 그래프 인식 레이어의 의미적 부분은 T5의 파라미터로 초기화한다.
- **결과**: SPIDER, SYN, DK, REALISTIC 등 네 개의 Text-To-SQL 벤치마크에서 최신 연구보다 우수한 성능을 보였다. 특히, GRAPHIX-T5-large는 T5-large보다 5.7%나 높은 정확도를 달성하였으며, T5-3B보다도 1.2% 높았다. 또한, 저자원 상황이나 복합 쿼리에 대해서도 GRAPHIX-T5가 구조적 편향을 도입함으로써 성능을 개선할 수 있음을 보였다.