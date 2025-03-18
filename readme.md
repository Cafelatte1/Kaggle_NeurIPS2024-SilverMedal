## 🏆 Kaggle NeurIPS2024 - Top5%(81th) SilverMedal Solution
![Python](https://img.shields.io/badge/Python-3.10-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Success-green)

## Introduction
- 특정 단백질 표적에 대한 소분자의 결합 친화도를 예측하는 모델을 개발하는 task
- 약물 유사 소분자(화학물질)가 세 가지 가능한 단백질 표적에 결합할지 예측하는 데 도움을 주어 약물 발견을 위한 길을 닦는데 기여하게 됨
- [Solution Link](https://www.kaggle.com/code/cafelatte1/81th-solution-1dcnn-with-all-data-feat-densenet)

## Dataset
- Protein Sequence
- 3가지 단백질 표적 결합 유무

## CV Strategy
- Target group별 층화추출 샘플링을 통한 검증시스템 구축
- 대용량데이터로 인해 holdout 전략 사용

## Preprocessing & Feature Engineering
- 아미노산을 개별 character처럼 취급하여 정수로 인코딩

## Modeling
- 아미노산을 하나의 token으로 취급하여 transformer 아키텍처를 통해 관계를 학습
- 1D Convolution Block을 통해 Molecule Smiles 분자 간의 관계를 학습시킨 후 Dense Block을 통해 최종 분류를 할 수 있도록 학습함

## Core Strategy
### 1. DenseNet Architecture
- 이미지 관련 Task에 주로 쓰이는 **DenseNet 아키텍처를 다른 Task에 차용해도 좋은 성능을 낼 수 있음을 증명**
![image](https://github.com/user-attachments/assets/31e1a682-99a3-4fe0-b6b6-a9eb3cc15705)
