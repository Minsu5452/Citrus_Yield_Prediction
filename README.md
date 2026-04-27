# 감귤 착과량 예측

제주 감귤 나무 생육 데이터를 기반으로 착과량을 예측한 DACON 회귀 경진대회 프로젝트입니다. 짧은 대회 기간 안에서 피처 구성, 모델 비교, multi K-fold ensemble을 빠르게 구성했습니다.

## 개요

| 항목 | 내용 |
| --- | --- |
| 대회 | 감귤 착과량 예측 AI 경진대회 |
| 기간 | 2022.12.12 - 2022.12.14 |
| 주최 / 주관 | 제주테크노파크 / DACON |
| 결과 | 17등, Top 6.6% |
| 과제 | 감귤 착과량 회귀 예측 |

## 접근

- 생육 정보에서 착과량 예측에 필요한 파생 변수를 구성했습니다.
- feature scaling과 selection 실험을 분리해 입력 피처 품질을 비교했습니다.
- XGBoost, LightGBM, CatBoost 기반 회귀 모델을 학습했습니다.
- seed와 fold를 달리한 multi K-fold ensemble로 예측 안정성을 높였습니다.

## 저장소 구성

```text
.
├── notebooks/
│   ├── 01_feature_engineering.ipynb
│   ├── 02_feature_scaling.ipynb
│   ├── 03_feature_selection.ipynb
│   ├── 04_multi_kfold_experiment.ipynb
│   └── 05_final_ensemble_solution.ipynb
├── reports/
│   └── citrus_yield_prediction_solution.pdf
└── requirements.txt
```

## 공개 범위

대회 원본 데이터와 제출 파일은 포함하지 않았습니다. 노트북 출력과 실행 메타데이터를 정리했습니다.

## 링크

- [DACON 대회 페이지](https://dacon.io/competitions/official/236038/overview/description)
- [DACON 코드 공유](https://dacon.io/competitions/official/236038/codeshare/7302)
