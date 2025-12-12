# Project 3: Recurrent Neural Network (RNN) from Scratch

본 프로젝트는 딥러닝 학부 강의의 세 번째 과제로,  
문장 데이터를 입력으로 받아 감정(이모지)을 예측하는  
**Recurrent Neural Network(RNN)**를  
**PyTorch, TensorFlow 등의 딥러닝 프레임워크 없이 NumPy만을 사용하여 직접 구현**한 프로젝트입니다.

시퀀스 데이터 처리, 은닉 상태 전달, 그리고  
Backpropagation Through Time(BPTT)을 코드 수준에서 구현하는 데 초점을 두었습니다.

---

## 🎯 Objectives
- 시퀀스 데이터를 처리하는 RNN 구조 이해
- Time step 단위의 hidden state 전파 방식 학습
- BPTT(Backpropagation Through Time) 직접 구현
- Word embedding 기반 자연어 입력 처리

---

## ⚙️ Key Features
- GloVe 기반 word embedding (50-dimension) 사용
- Vanilla RNN layer 직접 구현
  - 입력–은닉 상태–출력 흐름 설계
  - tanh 기반 hidden state 업데이트
- Multi-layer RNN 구조 구성
- Softmax + Cross-Entropy Loss 구현
- 문장 단위 감정(이모지) 분류 수행
- Training / Test loss 추적
- Test set 정확도 및 예측 이모지 출력

---

## 🛠 Implementation Overview
- 문장을 단어 단위로 분리한 후 GloVe embedding으로 변환
- 각 단어를 순차적으로 RNN에 입력하여 hidden state 업데이트
- 마지막 hidden state를 이용해 분류 결과 예측
- Softmax 출력을 통해 클래스 확률 계산
- Cross-Entropy Loss 기반 오차 계산
- BPTT를 통해 시간 축을 따라 gradient 전파
- Gradient를 이용해 가중치 및 bias 업데이트

---

## 🧠 What I Learned
- RNN이 시퀀스 데이터를 처리하는 방식과 hidden state의 역할을 명확히 이해함
- Time step이 증가할수록 gradient가 누적·전파되는 구조를 직접 구현하며  
  BPTT의 동작 원리를 체득
- MLP, CNN과 달리 순차적 의존성이 중요한 문제에서  
  RNN이 갖는 장점과 한계를 이해함
- 이후 LSTM으로 확장되는 구조의 필요성을 자연스럽게 인식함

---

## 📎 Notes
- 본 프로젝트는 교육 목적의 구현입니다.
- 문장 길이가 비교적 짧은 데이터셋을 사용하였으며,  
  장기 의존성 문제는 이후 LSTM 프로젝트에서 다룹니다.
