# Project 2: Convolutional Neural Network (CNN) from Scratch

본 프로젝트는 딥러닝 학부 강의의 두 번째 과제로,  
MNIST 데이터셋을 대상으로 **Convolutional Neural Network(CNN)**를  
**PyTorch, TensorFlow 등의 딥러닝 프레임워크 없이 NumPy만을 사용하여 직접 구현**한 프로젝트입니다.

Convolution 연산, Pooling, Flatten, Fully Connected layer까지  
CNN을 구성하는 핵심 연산들을 모두 수식과 코드 수준에서 구현하였습니다.

---

## 🎯 Objectives
- CNN 구조와 동작 원리 이해
- Convolution 및 Pooling 연산의 forward / backward 과정 구현
- MLP 대비 CNN의 표현력 차이 이해
- 프레임워크 없이 CNN 학습 파이프라인 구성

---

## ⚙️ Key Features
- MNIST 데이터셋 직접 로딩 (`.gz` 파일 처리)
- Mini-batch 기반 데이터 로더 구현
- CNN 네트워크 구성
  - Convolution → ReLU → Max Pooling
  - Convolution → ReLU → Max Pooling
  - Flatten → Fully Connected → Softmax
- `im2col / col2im` 방식을 활용한 Convolution 구현
- ReLU 및 Softmax 활성화 함수 직접 구현
- Cross-Entropy Loss 기반 학습
- SGD 기반 파라미터 업데이트
- Training / Test loss 추적
- Confusion Matrix 및 클래스별 Top-3 예측 결과 분석

---

## 🛠 Implementation Overview
- 입력 이미지를 (N, C, H, W) 형태로 처리
- `im2col`을 통해 Convolution 연산을 행렬 곱으로 변환하여 계산
- Max Pooling layer에서 공간적 특징 요약
- Flatten layer를 통해 Fully Connected layer 입력 구성
- Softmax 출력을 통해 클래스 확률 계산
- Backpropagation을 통해 Convolution, Pooling, FC layer의 gradient 계산
- SGD를 이용한 가중치 업데이트

---

## 🧠 What I Learned
- CNN에서 Convolution과 Pooling이 수행하는 역할을 코드 수준에서 이해함
- Convolution 연산을 행렬 연산으로 변환하는 `im2col` 기법의 장점 체득
- MLP 대비 CNN이 이미지 데이터에 더 적합한 이유를 실험적으로 이해함
- 딥러닝 프레임워크가 제공하는 CNN 연산의 내부 동작을 명확히 파악함

---

## 📎 Notes
- 본 프로젝트는 교육 목적의 구현입니다.
- 계산 효율보다는 CNN 구조와 학습 원리 이해에 초점을 두었습니다.
