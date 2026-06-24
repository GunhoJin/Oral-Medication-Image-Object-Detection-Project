# Oral Medication Image Object Detection Project

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Colab](https://img.shields.io/badge/Google%20Colab-supported-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)

> Detect pills in medication photos and turn them into structured healthcare information.

## Overview

This project is a beginner-level object detection mission for a healthcare scenario.
The goal is to detect up to four pills in an image and predict each pill's class with a bounding box.

### What the notebook does

- Mounts Google Drive in Colab
- Loads merged annotation JSON files
- Builds a dataframe from image and annotation records
- Remaps category IDs for training
- Checks class imbalance
- Checks the number of pills per image
- Analyzes bounding box sizes
- Draws boxes on sample images for visual QA

## Results & Findings

The current notebook focuses on exploratory analysis rather than final model training metrics.

### What is currently verified

- Class distribution across the 73 categories
- Number of pills per image
- Bounding box area distribution
- Visual sanity checks with sample images

### What is not yet documented here

- Final training score
- Kaggle leaderboard score
- Test-time inference metrics

If you add a trained baseline later, this section is the right place for:

- mAP
- precision / recall
- loss curves
- comparison against previous runs

## Project Context

Imagine a healthcare startup team called **Health Eat**.

The product idea is simple:

- A user takes a photo of their medication
- The model detects pills and identifies them
- The app can then present medication information and safety guidance

## Dataset Notes

- The task uses merged COCO-style annotations
- The notebook references 73 classes
- The mission states that each image may contain up to 4 pills
- Training and test image folders are handled separately in the notebook

## Tech Stack

- Python
- PyTorch
- TorchVision
- Pandas
- Pillow
- OpenCV
- Matplotlib
- Seaborn
- Google Colab

## Repository Contents

| File | Description |
| --- | --- |
| `README.md` | Project overview and usage guide |
| `LICENSE` | MIT License |
| `test.ipynb` | Main notebook for data analysis and model preparation |

## Notebook Flow

1. Mount Google Drive
2. Normalize Korean paths
3. Load merged annotation JSON files
4. Convert annotations into a dataframe
5. Map category IDs for model training
6. Plot class distribution
7. Count pills per image
8. Inspect bounding box areas
9. Visualize samples with bounding boxes

## How to Run

Open `test.ipynb` in Google Colab or Jupyter and run the cells in order.

Typical setup:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Then update the dataset path inside the notebook to match your environment.

## Roadmap

- Train a baseline detector
- Tune augmentation and anchor settings
- Add validation metrics
- Export submission files for Kaggle-style evaluation
- Add sample screenshots to the README

## License

MIT License. See [LICENSE](LICENSE) for details.

---

# 구강 복용 약물 이미지 객체 탐지 프로젝트

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Colab](https://img.shields.io/badge/Google%20Colab-supported-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)

> 약 사진에서 알약을 탐지해 구조화된 헬스케어 정보로 바꾸는 프로젝트입니다.

## 개요

이 프로젝트는 헬스케어 시나리오를 위한 초급 객체 탐지 미션입니다.
한 장의 이미지에서 최대 4개의 알약을 탐지하고, 각 알약의 클래스와 바운딩 박스를 예측하는 것이 목표입니다.

### 노트북이 하는 일

- Colab에서 Google Drive 마운트
- 병합된 annotation JSON 로드
- 이미지와 어노테이션으로 데이터프레임 생성
- 학습용 category ID 재매핑
- 클래스 불균형 확인
- 이미지당 알약 개수 확인
- 바운딩 박스 크기 분석
- 샘플 이미지에 박스 시각화

## 결과 및 확인 사항

현재 노트북은 최종 학습 점수보다 탐색적 분석에 초점이 있습니다.

### 지금 확인된 내용

- 73개 클래스의 분포
- 이미지당 알약 개수
- 바운딩 박스 면적 분포
- 샘플 이미지 시각 검증

### 아직 여기에는 없는 내용

- 최종 학습 성능
- Kaggle 리더보드 점수
- 테스트 시점 추론 지표

나중에 기준 모델을 학습하면 여기에 다음 항목을 넣는 것이 좋습니다.

- mAP
- precision / recall
- loss curve
- 이전 실험과의 비교

## 프로젝트 배경

이 프로젝트는 **헬스잇(Health Eat)** 이라는 헬스케어 스타트업 팀 상황을 가정합니다.

서비스 아이디어는 다음과 같습니다.

- 사용자가 복용 중인 약을 사진으로 찍는다
- 모델이 알약을 탐지하고 식별한다
- 앱이 약물 정보를 안내한다

## 데이터 참고 사항

- 병합된 COCO 형식 annotation을 사용합니다
- 노트북 기준 클래스 수는 73개입니다
- 미션상 이미지당 최대 4개의 알약을 다룹니다
- 학습 이미지와 테스트 이미지를 분리해서 사용합니다

## 사용 기술

- Python
- PyTorch
- TorchVision
- Pandas
- Pillow
- OpenCV
- Matplotlib
- Seaborn
- Google Colab

## 저장소 구성

| 파일 | 설명 |
| --- | --- |
| `README.md` | 프로젝트 설명과 사용 방법 |
| `LICENSE` | MIT 라이선스 |
| `test.ipynb` | 데이터 분석 및 모델 준비용 메인 노트북 |

## 노트북 흐름

1. Google Drive 마운트
2. 한글 경로 정규화
3. 병합된 annotation JSON 로드
4. 어노테이션을 데이터프레임으로 변환
5. category ID를 학습용으로 재매핑
6. 클래스 분포 시각화
7. 이미지당 알약 개수 계산
8. 바운딩 박스 면적 확인
9. 샘플 이미지 박스 시각화

## 실행 방법

`test.ipynb`를 Google Colab 또는 Jupyter에서 열고 셀을 순서대로 실행합니다.

기본 설정 예시:

```python
from google.colab import drive
drive.mount('/content/drive')
```

그 다음 노트북의 데이터 경로를 자신의 환경에 맞게 수정하면 됩니다.

## 다음 단계

- 기준 객체 탐지 모델 학습
- 데이터 증강 및 앵커 설정 조정
- 검증 지표 추가
- Kaggle 제출 파일 생성
- README에 스크린샷 추가

## 라이선스

MIT License입니다. 자세한 내용은 [LICENSE](LICENSE)를 확인하세요.
