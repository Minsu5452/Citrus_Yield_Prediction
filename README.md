# Citrus Yield Prediction

제주 감귤 착과량 예측 DACON 대회 저장소입니다. 짧은 대회 기간 안에 feature engineering과 multi K-fold ensemble을 구성해 257팀 중 17위를 기록했습니다.

## Snapshot

| Item | Detail |
| --- | --- |
| Type | Competition solution |
| Period | 2022.12 |
| Team | 3 people, team lead |
| Result | 17th / 257 teams, top 6.6% |
| Task | 감귤 착과량 회귀 예측 |
| Key approach | XGBoost, LightGBM, CatBoost, multi K-fold blending |

## Contribution

- 짧은 일정 안에 EDA와 검증 파이프라인을 먼저 정리했습니다.
- 나무 단위 집계와 비율 파생 변수를 중심으로 feature set을 구성했습니다.
- seed를 달리한 multi K-fold 실험으로 fold 편향을 줄였습니다.
- 세 가지 boosting 모델을 조합해 안정적인 앙상블 예측을 만들었습니다.

## Repository Layout

- `Feature/`: scaling, selection, feature set 정리 노트북
- `Kfold/`: multi K-fold 실험 노트북
- `[Private 17위] XGBoost + LightGBM + Catboost Multi KFold Ensembles.ipynb`: 최종 제출 노트북
- `[Private 17위] XGBoost + LightGBM + Catboost Multi KFold Ensembles.pdf`: 솔루션 자료

## Links

- [DACON competition page](https://dacon.io/competitions/official/236038/overview/description)
