# Citrus Yield Prediction

제주 감귤 나무의 생육 데이터를 기반으로 착과량을 예측한 DACON 회귀 경진대회 프로젝트입니다. 짧은 대회 기간 안에 feature engineering, scaling/selection 실험, multi K-fold ensemble을 구성해 257팀 중 17위를 기록했습니다.

## Overview

| 항목 | 내용 |
| --- | --- |
| 대회 | 감귤 착과량 예측 AI 경진대회 |
| 기간 | 2022.12.12 ~ 2022.12.14 |
| 주최 | 제주테크노파크 |
| 주관 | DACON |
| 팀 구성 | 3인팀, 팀장 |
| 결과 | 17위 / 257팀 |
| 과제 | 감귤 착과량 회귀 예측 |

## Approach

- 나무 생육 정보에서 착과량 예측에 사용할 파생 변수를 구성했습니다.
- Feature scaling과 feature selection 실험을 분리해 모델 입력 품질을 비교했습니다.
- XGBoost, LightGBM, CatBoost 기반 회귀 모델을 학습했습니다.
- seed와 fold를 달리한 multi K-fold ensemble로 예측 안정성을 높였습니다.

## Repository Structure

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
├── requirements.txt
└── README.md
```

## Public Scope

이 저장소는 포트폴리오 공개용으로 정리한 버전입니다.

- 대회 제공 데이터와 제출 CSV는 포함하지 않았습니다.
- 노트북 출력 결과와 실행 메타데이터는 제거했습니다.
- 실행하려면 DACON 대회 데이터를 `data/` 경로에 별도로 배치해야 합니다.

## Links

- [DACON competition page](https://dacon.io/competitions/official/236038/overview/description)
- [DACON code share: Private 17th solution](https://dacon.io/competitions/official/236038/codeshare/7302)
