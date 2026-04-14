# AIFFEL Campus Online Code Peer Review Templete
- 코더 : 정수연
- 리뷰어 : 정주열


# PRT(Peer Review Template)
- [x]  **1. 주어진 문제를 해결하는 완성된 코드가 제출되었나요?**
    - 문제에서 요구하는 최종 결과물이 첨부되었는지 확인
        - SentencePiece 모델 학습, sp_tokenize() 구현, LSTM 모델 학습 및 평가, Mecab 비교, BPE 옵션 변경 실험까지 전체 파이프라인이 구현되어 있습니다.
    <img width="1188" height="490" alt="image" src="https://github.com/user-attachments/assets/d0917dc1-15eb-4be4-af13-10b3712dc320" />
    <img width="1201" height="492" alt="image" src="https://github.com/user-attachments/assets/9922243e-976d-47b1-a32b-b93a91e7be33" />

- [x]  **2. 전체 코드에서 가장 핵심적이거나 가장 복잡하고 이해하기 어려운 부분에 작성된 
주석 또는 doc string을 보고 해당 코드가 잘 이해되었나요?**
    - 해당 코드 블럭을 왜 핵심적이라고 생각하는지 확인
    - 해당 코드 블럭에 doc string/annotation이 달려 있는지 확인
    - 해당 코드의 기능, 존재 이유, 작동 원리 등을 기술했는지 확인
    - 주석을 보고 코드 이해가 잘 되었는지 확인
        - 데이터 전처리 부분에서 과정과 파라미터를 주석으로 써주셔서 이해하기 좋았습니다.
        - `load_data_sp()` 함수도 기존 Mecab 방식과 SentencePiece 방식의 차이를 주석으로 비교한 부분이 인상적이었습니다.
        <img width="444" height="453" alt="image" src="https://github.com/user-attachments/assets/56a1d735-47ba-4789-bfe3-7c77e1ef3233" />
        <img width="649" height="344" alt="image" src="https://github.com/user-attachments/assets/4c410389-151b-4c7f-8b7c-22268d94c453" />

- [ ]  **3. 에러가 난 부분을 디버깅하여 문제를 해결한 기록을 남겼거나
새로운 시도 또는 추가 실험을 수행해봤나요?**
    - 문제 원인 및 해결 과정을 잘 기록하였는지 확인
    - 프로젝트 평가 기준에 더해 추가적으로 수행한 나만의 시도, 
    실험이 기록되어 있는지 확인
        - BPE 모델 타입 변경 실험을 추가로 수행한 점은 좋았습니다.
        - 그러나 모든 모델에서 Loss가 줄어들지 않는 문제가 발생했는데, 이에 대한 원인 분석이나 디버깅 과정이 기록되지 않았습니다.
    <img width="1191" height="487" alt="image" src="https://github.com/user-attachments/assets/006364db-f6ce-41d3-838b-43d5505d324d" />

- [x]  **4. 회고를 잘 작성했나요?**
    - 주어진 문제를 해결하는 완성된 코드 내지 프로젝트 결과물에 대해
    배운점과 아쉬운점, 느낀점 등이 기록되어 있는지 확인
    - 전체 코드 실행 플로우를 그래프로 그려서 이해를 돕고 있는지 확인
        - SentencePiece와 Word2Vec의 차이점, 각각의 장단점을 정리한 부분이 좋았습니다.
    <img width="984" height="193" alt="image" src="https://github.com/user-attachments/assets/f6eab34a-8f98-45d3-8427-46619998cb34" />

- [x]  **5. 코드가 간결하고 효율적인가요?**
    - 파이썬 스타일 가이드 (PEP8) 를 준수하였는지 확인
    - 코드 중복을 최소화하고 범용적으로 사용할 수 있도록 함수화/모듈화했는지 확인
        - `load_data_sp()`, `sp_tokenize()`, `train()`, `test()` 등 함수화가 잘 되어 있습니다.
    <img width="358" height="167" alt="image" src="https://github.com/user-attachments/assets/b05e9a3a-01f0-4dc1-94c7-5b7da5ef6f2c" />
    <img width="634" height="206" alt="image" src="https://github.com/user-attachments/assets/93467224-f50e-49af-b3c2-252b069c24f8" />

# 회고(참고 링크 및 코드 개선)
전체적으로 SentencePiece 학습 → sp_tokenize 구현 → 모델 학습 → Mecab 비교 → BPE 옵션 변경까지 프로젝트 흐름은 잘 잡혀있습니다. 모델이 수렴하지 않았던 부분에서 어디서 문제가 발생했는지 빨리 발견해서 해결되셨으면 좋겠습니다.
