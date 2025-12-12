# Project 1: Multilayer Perceptron (MLP) from Scratch

본 프로젝트는 딥러닝 학부 강의에서 수행한 과제로,  
MNIST 데이터셋을 대상으로 **Multilayer Perceptron(MLP)** 신경망을  
**PyTorch, TensorFlow 등의 딥러닝 프레임워크 없이 NumPy만을 사용하여 직접 구현**하였습니다.

데이터 로딩부터 순전파, 역전파, 파라미터 업데이트까지  
신경망 학습의 전 과정을 코드 수준에서 구현하는 데 초점을 두었습니다.

---

## 🎯 Objectives
- MLP 구조와 학습 원리 이해
- Forward / Backward Propagation 직접 구현
- 활성화 함수, 손실 함수의 역할 이해
- 프레임워크 없이 신경망 학습 파이프라인 구성

---

## ⚙️ Key Features
- MNIST 데이터셋 직접 로딩 (`.gz` 파일 처리)
- Mini-batch 기반 데이터 로더 구현
- 3-layer MLP 구조
  - Linear → ReLU → Linear → ReLU → Linear → Softmax
- ReLU, Softmax 활성화 함수 직접 구현
- Cross-Entropy Loss 구현
- Stochastic Gradient Descent(SGD) 기반 학습
- Training / Test loss 추적 및 시각화
- Confusion Matrix 및 클래스별 Top-3 예측 샘플 분석

---

## 🛠 Implementation Overview
- 입력 이미지를 벡터 형태(28×28 → 784)로 변환하여 MLP에 입력
- 각 Linear layer에서 가중치 및 bias 연산 수행
- ReLU 활성화를 통한 비선형성 부여
- Softmax 출력을 통해 클래스 확률 계산
- Cross-Entropy Loss를 기반으로 오차 계산
- Backpropagation을 통해 각 layer의 gradient 계산
- SGD 방식으로 가중치 및 bias 업데이트

---

## 🧠 What I Learned
- MLP의 forward / backward 연산 흐름을 수식과 코드로 명확히 이해함
- 활성화 함수와 손실 함수가 학습 안정성에 미치는 영향 체득
- 딥러닝 프레임워크가 내부적으로 수행하는 연산을  
  직접 구현하며 추상화된 개념을 구체적으로 이해함
- CNN, RNN, LSTM으로 확장되는 딥러닝 모델 학습의 기초 확립

---

## 📎 Notes
- 본 프로젝트는 교육 목적의 구현입니다.
- 계산 효율이나 최적화보다는 구조와 동작 원리의 이해에 초점을 두었습니다.
