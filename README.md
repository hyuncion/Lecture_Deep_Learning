# Deep Learning Projects (from Scratch with NumPy)

본 저장소는 **딥러닝 학부 강의**를 수강하며 진행한 프로젝트들을 정리한 것입니다.  
MLP, CNN, RNN, LSTM 모델을 **PyTorch나 TensorFlow와 같은 딥러닝 프레임워크를 사용하지 않고**,  
**NumPy만을 이용하여 신경망을 직접 구현**하였습니다.

각 프로젝트에서는 순전파(Forward Propagation), 역전파(Backpropagation),  
손실 함수, 최적화 기법 등 딥러닝의 핵심 구성 요소를 수식과 코드 수준에서 구현하는 데 초점을 두었습니다.

---

## 📌 Project Overview

### 🔹 Project 1. MLP (Multilayer Perceptron)
- 3-layer MLP를 NumPy만으로 구현
- Linear layer, ReLU, Softmax, Cross-Entropy Loss 직접 구현
- SGD 기반 학습 파이프라인 구성
- MNIST 데이터셋을 이용한 이미지 분류 수행

---

### 🔹 Project 2. CNN (Convolutional Neural Network)
- Convolution layer, Max Pooling layer를 NumPy로 직접 구현
- Convolution 연산의 forward / backward 과정 구현
- MLP 대비 CNN 구조의 성능 차이 분석
- MNIST 데이터셋 기반 이미지 분류

---

### 🔹 Project 3. RNN (Recurrent Neural Network)
- Vanilla RNN을 NumPy로 직접 구현
- 시퀀스 데이터를 처리하는 순환 구조 학습
- Word embedding 기반 문장 입력 처리
- 감정(이모지) 분류 태스크 수행

---

### 🔹 Project 4. LSTM (Long Short-Term Memory)
- LSTM 셀 구조 및 gate 연산 직접 구현
- Gradient vanishing 문제 완화 메커니즘 학습
- RNN과 LSTM 성능 비교
- Optimizer(SGD, Adam), Dropout, Embedding 차원(50d / 100d)에 따른 성능 분석

---

## 🧠 Learning Objectives
- 딥러닝 모델의 내부 동작 원리를 프레임워크 없이 이해
- Forward / Backward propagation의 수식적 의미를 코드로 구현
- CNN, RNN, LSTM 구조의 차이와 사용 목적 이해
- Optimizer, Dropout, Embedding 기법이 성능에 미치는 영향 분석

---

## 🛠 Implementation Notes
- 사용 라이브러리: **Python, NumPy**
- 딥러닝 프레임워크(PyTorch, TensorFlow 등)는 사용하지 않음
- 모든 layer, loss, optimizer를 직접 구현
- 학습 및 평가 파이프라인을 프로젝트별로 구성

---

## 📎 Notes
- 본 프로젝트들은 교육 목적의 구현입니다.
- 실제 프레임워크 기반 구현과는 성능 및 효율성에서 차이가 있을 수 있습니다.
- 각 프로젝트 폴더에는 개별 README를 통해 상세한 설명을 제공합니다.
