# Project 4: Long Short-Term Memory (LSTM) from Scratch

본 프로젝트는 딥러닝 학부 강의의 네 번째 과제로,  
문장 데이터를 입력으로 받아 감정(이모지)을 분류하는  
**Long Short-Term Memory(LSTM)** 네트워크를  
**PyTorch, TensorFlow 등의 딥러닝 프레임워크 없이 NumPy만을 사용하여 직접 구현**한 프로젝트입니다.

Vanilla RNN의 한계인 gradient vanishing 문제를 해결하기 위한  
LSTM의 gate 구조와 cell state 동작을 코드 수준에서 구현하는 데 초점을 두었습니다.

---

## 🎯 Objectives
- LSTM 구조 및 동작 원리 이해
- Forget / Input / Output gate의 역할 학습
- Cell state를 통한 장기 의존성 처리 방식 이해
- RNN과 LSTM의 구조적 차이 비교

---

## ⚙️ Key Features
- GloVe 기반 word embedding 사용
  - 50-dimension / 100-dimension 비교
- LSTM layer 직접 구현
  - Forget gate, Input gate, Output gate, Cell state 계산
- Multi-layer LSTM 구조 구성
- Softmax + Cross-Entropy Loss 구현
- 다양한 학습 설정 실험
  - Optimizer: SGD, Adam
  - Dropout 적용 여부
- Training / Test loss 추적
- Test set 정확도 및 예측 이모지 출력

---

## 🛠 Implementation Overview
- 문장을 단어 단위로 분리한 후 GloVe embedding으로 변환
- 각 단어를 순차적으로 LSTM 셀에 입력하여 hidden state와 cell state 갱신
- Gate 연산을 통해 정보의 유지 및 제거 여부 결정
- 마지막 hidden state를 이용해 분류 결과 예측
- Cross-Entropy Loss 기반 오차 계산
- Time step을 따라 역전파를 수행하며 gradient 계산
- Optimizer(SGD / Adam)를 이용한 파라미터 업데이트
- Dropout을 적용하여 과적합 완화 실험

---

## 🧠 What I Learned
- LSTM의 gate 구조가 장기 의존성 문제를 어떻게 완화하는지 명확히 이해함
- RNN 대비 LSTM이 안정적인 학습 성능을 보이는 이유를 실험적으로 확인함
- Optimizer(SGD, Adam)와 embedding 차원(50d, 100d)이 성능에 미치는 영향 체득
- 복잡한 순환 신경망 구조를 프레임워크 없이 구현하며  
  딥러닝 모델 내부 동작에 대한 깊은 이해를 얻음

---

## 📎 Notes
- 본 프로젝트는 교육 목적의 구현입니다.
- 계산 효율보다는 LSTM 구조와 학습 원리 이해에 초점을 두었습니다.
