# Oral Medication Image Object Detection Project

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Colab](https://img.shields.io/badge/Google%20Colab-supported-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)

An object detection project for recognizing oral medication images in a healthcare scenario.

This repo is built around a beginner mission: detect up to 4 pills in a photo and classify each pill with a bounding box.

## Project Overview

Imagine a healthcare startup team called **Health Eat**.

The goal is to build a model that can:

- Detect pills in a user-uploaded image
- Classify each pill
- Return bounding boxes for the detected objects
- Support a healthcare use case where medication information can be shown to users

The notebook currently focuses on:

- Loading merged COCO-style annotations
- Building a training dataframe
- Mapping category IDs for model training
- Checking class imbalance
- Checking the number of pills per image
- Analyzing bounding box sizes
- Visual QA by drawing boxes on sample images

## Dataset Notes

- The task uses a merged annotation format
- The notebook references 73 classes
- The mission states that each image may contain up to 4 pills
- Train and test image folders are handled separately in the notebook

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

## Notebook Workflow

1. Mount Google Drive in Colab
2. Normalize paths for Korean directory names
3. Load merged annotation JSON files
4. Build a dataframe from image and annotation records
5. Remap category IDs for model training
6. Plot class distribution
7. Check pills per image
8. Analyze bounding box area distribution
9. Visualize real images with bounding boxes

## How to Run

Open `test.ipynb` in Google Colab or Jupyter, then follow the notebook cells in order.

Typical setup flow:

```python
from google.colab import drive
drive.mount('/content/drive')
```

Then update the dataset path inside the notebook to match your environment.

## Example Output Checks

- Class imbalance plot
- Pills per image distribution
- Bounding box size histogram
- Sample image visualization with boxes

## Roadmap

Possible next steps for this project:

- Train a baseline detector
- Tune augmentation and anchor settings
- Add evaluation metrics
- Export submission files for Kaggle-style validation

## License

MIT License. See [LICENSE](LICENSE) for details.

---

# 구강 복용 약물 이미지 객체 탐지 프로젝트

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Colab](https://img.shields.io/badge/Google%20Colab-supported-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)

헬스케어 환경에서 복용 중인 약 사진을 인식하는 객체 탐지 프로젝트입니다.

초급 미션 기준으로, 한 장의 이미지에서 최대 4개의 알약을 탐지하고 각 객체의 위치와 클래스를 예측하는 것이 목표입니다.

## 프로젝트 개요

이 프로젝트는 **헬스잇(Health Eat)** 이라는 헬스케어 스타트업 팀 상황을 가정합니다.

목표는 다음과 같습니다.

- 사용자가 업로드한 약 사진에서 알약을 탐지
- 각 알약의 클래스를 분류
- 바운딩 박스를 함께 예측
- 복약 정보 제공을 위한 헬스케어 활용 시나리오에 적용

현재 노트북은 주로 아래 작업을 수행합니다.

- 병합된 COCO 형식 어노테이션 로드
- 학습용 데이터프레임 생성
- 모델 학습용 category ID 매핑
- 클래스 불균형 확인
- 이미지당 알약 개수 확인
- 바운딩 박스 크기 분석
- 샘플 이미지에 박스를 그려 시각적 검증

## 데이터 참고 사항

- 병합된 annotation JSON 형식을 사용합니다
- 노트북 기준 클래스 수는 73개입니다
- 미션상 이미지당 최대 4개의 알약을 다룹니다
- 학습용 이미지와 테스트용 이미지를 분리해서 사용합니다

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

## 노트북 진행 흐름

1. Colab에서 Google Drive 마운트
2. 한글 경로를 위해 경로 문자열 정규화
3. 병합된 annotation JSON 파일 로드
4. 이미지와 어노테이션 정보를 데이터프레임으로 변환
5. category ID를 학습용으로 재매핑
6. 클래스 분포 시각화
7. 이미지당 알약 개수 확인
8. 바운딩 박스 면적 분포 확인
9. 샘플 이미지에 박스 시각화

## 실행 방법

`test.ipynb`를 Google Colab 또는 Jupyter에서 열고 순서대로 실행합니다.

기본 예시는 다음과 같습니다.

```python
from google.colab import drive
drive.mount('/content/drive')
```

그 다음 노트북 안의 데이터셋 경로를 자신의 환경에 맞게 수정하면 됩니다.

## 확인 가능한 예시 결과

- 클래스 불균형 그래프
- 이미지당 알약 개수 분포
- 바운딩 박스 크기 히스토그램
- 박스가 그려진 샘플 이미지

## 다음 단계

이 프로젝트의 다음 작업 후보는 다음과 같습니다.

- 기준 객체 탐지 모델 학습
- 데이터 증강 및 앵커 설정 조정
- 평가 지표 추가
- Kaggle 제출 파일 생성

## 라이선스

MIT License입니다. 자세한 내용은 [LICENSE](LICENSE)를 확인하세요.
