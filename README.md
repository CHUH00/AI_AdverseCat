<div align="center">

# 🐱 AI AdverseCat: 텐서플로우(TensorFlow)를 활용한 적대적 공격
### 🛡️ 딥러닝 모델의 취약성 및 강건성(Robustness) 연구

![TensorFlow](https://img.shields.io/badge/TensorFlow-%23FF6F00.svg?style=for-the-badge&logo=TensorFlow&logoColor=white)
![Keras](https://img.shields.io/badge/Keras-%23D00000.svg?style=for-the-badge&logo=Keras&logoColor=white)
![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

</div>

## 📌 프로젝트 소개
**AI AdverseCat**은 사전 학습된 이미지 분류 모델에 대한 **적대적 공격(Adversarial Attacks)**을 직접 구현하고 실험하는 딥러닝 연구 프로젝트입니다. 정확도가 매우 높은 신경망이라 할지라도, 인간의 눈에는 보이지 않는 정교한 노이즈(섭동)를 추가하면 쉽게 속일 수 있습니다.

본 노트북은 **TensorFlow와 Keras**를 활용하여 ImageNet 데이터셋으로 학습된 분류기가 어떻게 결정을 내리는지 분석합니다. 또한, 대표적인 적대적 변형 기법(FGSM - Fast Gradient Sign Method)을 적용해 딥러닝 모델이 일반적인 강아지 사진을 고양이 등으로 완전히 잘못 분류하도록 유도하는 과정을 시각적으로 보여줍니다.

## ✨ 주요 기능
- **취약성 검증**: 적대적 학습이 되어 있지 않은 일반적인 합성곱 신경망(CNN)이 계산된 노이즈 공격에 얼마나 취약한지 증명합니다.
- **기울기 기반 공격 (Gradient-Based Attacks)**: 오차 역전파를 통해 모델 가중치가 아닌 *입력 이미지 픽셀 자체*에 대한 기울기를 계산하여 노이즈 맵을 생성합니다.
- **ImageNet 통합 매핑**: 대규모 분류 작업을 시뮬레이션하기 위해 실제 현실의 클래스 매핑 구조(`imagenet_classes.json`)를 사용합니다.
- **시각적 해석 가능성**: `matplotlib`을 이용해 원본 이미지, 추출된 노이즈 레이어, 그리고 모델을 속인 최종 적대적 생성 이미지를 직관적으로 비교할 수 있습니다.

## 🛠️ 기술 스택
* **프레임워크**: `TensorFlow` & `Keras`
* **데이터 처리**: `NumPy`
* **이미지 처리**: `Pillow (PIL)`
* **시각화**: `Matplotlib`
* **개발 환경**: `Jupyter Notebook`

## 🚀 실행 방법

### 요구 환경
Python 3.8 이상과 함께 다음 라이브러리들이 필요합니다:
```bash
pip install tensorflow numpy matplotlib pillow jupyter
```

### 노트북 실행
1. 로컬 환경에 저장소를 클론합니다.
   ```bash
   git clone https://github.com/CHUH00/AI_AdverseCat.git
   cd AI_AdverseCat
   ```
2. 주피터 노트북을 실행합니다.
   ```bash
   jupyter notebook
   ```
3. `AdversarialCat_TF.ipynb` 파일을 열고 셀을 순차적으로 실행하여 적대적 공격 과정을 실시간으로 확인해 보세요!

---
*본 프로젝트는 인공지능, 딥러닝 및 컴퓨터 비전 분야에 대한 끊임없는 탐구의 일환으로 [우진(Woojin Choi)](https://github.com/CHUH00)에 의해 개발되었습니다.*
