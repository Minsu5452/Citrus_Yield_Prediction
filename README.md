# 🍊 Citrus Yield Prediction — 감귤 착과량 예측 AI

![Rank](https://img.shields.io/badge/17th-257%20teams-brightgreen)
![Percentile](https://img.shields.io/badge/상위%206.6%25-top%20tier-success)
![Competition](https://img.shields.io/badge/DACON-Official%20Competition-blue)
![Host](https://img.shields.io/badge/Host-제주%20테크노파크-orange)
![Model](https://img.shields.io/badge/Model-XGBoost%20%2B%20LightGBM%20%2B%20CatBoost-red)

> **17th / 257팀 (상위 6.6%)** — 제주 감귤 농가의 수확량을 트리·잎·개화 데이터로 예측. **3-boosting 앙상블(XGBoost + LightGBM + CatBoost)** × **Multi K-Fold** 전략으로 안정적 일반화 성능 달성.

---

## 🏆 Award

- 🏅 **17위 / 257팀 (상위 6.6%)** · DACON · 2022.12.12 ~ 2022.12.14 (단기 대회)
- 주최: 제주테크노파크 / 주관: DACON

## 🔍 Overview

- **배경**: 농가 수확량 예측은 재배·유통·보험 전반의 기반 정보. 특히 감귤은 제주 지역 핵심 작물로 생산량 변동이 큰 작물.
- **문제 정의**: 나무별 잎·열매·개화 수 등 관측 데이터 + 환경 변수로 **총 착과량(regression) 예측**.
- **단기 대회 특성**: 2박 3일 시한 → **빠른 EDA + 검증 파이프라인 구축**이 승부처.

## 🧠 Approach

### 핵심 전략
- **3-way Boosting 앙상블**: XGBoost / LightGBM / CatBoost
  - 각 모델이 서로 다른 tree 분할 방식 → 다양성 확보
- **Multi K-Fold Ensembling**: 서로 다른 fold seed로 반복 CV → 단일 fold 편향 완화
- **Feature Engineering**:
  - 나무 단위 집계 피처
  - 개화·잎·열매 비율 파생 변수
  - 농가·품종 범주 encoding

### 파이프라인
```
Raw tree observations
    │
    ▼  Feature Engineering
- 나무별 집계
- 개화/잎/열매 비율
- 범주형 encoding
    │
    ▼  Multi K-Fold (5+ fold seeds)
균형 잡힌 검증셋
    │
    ▼  XGBoost ─┐
       LightGBM ─┼── Blending
       CatBoost ─┘
    │
    ▼  Final Prediction
```

## 📈 Results

| 리더보드 | 순위 | 비고 |
|---------|------|------|
| **Private** | **17위** | 257팀 중 상위 6.6% |

## 🛠 Tech Stack

- **Language**: Python 3.8+
- **ML**: XGBoost · LightGBM · CatBoost · scikit-learn
- **Data**: Pandas · NumPy
- **Env**: Jupyter Notebook

## 📁 Structure

```
Citrus_Yield_Prediction/
├── Feature/                                              # 피처 엔지니어링
├── Kfold/                                                # Multi K-Fold 실험
├── [Private 17위] XGBoost + LightGBM + Catboost Multi KFold Ensembles.ipynb
├── [Private 17위] ...pdf                                 # 최종 솔루션 리포트
└── README.md
```

## 👤 Role / Team

- **역할**: 팀장 (3인 팀)
- **기여**: 피처 엔지니어링 · K-Fold 전략 설계 · 3-way 앙상블 blending

## 🔗 Links

- [DACON 대회 페이지](https://dacon.io/competitions/official/236038/overview/description)

---

> 🔗 Portfolio: [Minsu5452](https://github.com/Minsu5452)
