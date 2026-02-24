# 🎯 BDA (수료율/완료 여부) 예측 AI 모델 개발

## Project Overview
- 학생/참가자 데이터를 사용하여 **완료 여부(Completion / Dropout)** 예측
- 기간:  2026.01.12 ~ 2026.02.23
- 팀 프로젝트 (4인)

## Data Preprocessing
- 범주형 변수의 cardinality가 높은 컬럼 정리
- 정보량이 낮거나 중복되는 변수 제거
- 파생변수 생성 및 결측 처리

## Modeling
- 최종 모델: **CatBoost**
- 여러 모델(LightGBM 등) 비교 실험 진행
- CV 성능이 가장 안정적이었던 CatBoost를 베이스 모델로 선정

## Ensemble Strategy
- **Multi-seed + Cross Validation 앙상블**
  - 서로 다른 seed로 학습하여 variance 감소
  - Fold별 예측 평균을 통해 안정성 확보
- Threshold 미세 튜닝을 통해 F1 Score 최적화

## Results
- Public Rank: 60th
- Private Rank: 28th
- Final Standing: 28 / 1,159 (Top 4%)

## Key Insight
- 단일 모델 대비 multi-seed 앙상블이 CV 분산을 줄이고 성능 안정화
- threshold 조정을 통해 최종 성능에 도달
- feature engineering보다 모델 안정화 전략이 더 중요한 역할을 함

https://dacon.io/competitions/official/236664/overview/description
