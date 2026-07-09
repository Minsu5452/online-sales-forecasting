# 온라인 채널 제품 판매량 예측 해커톤

[![Python](https://img.shields.io/badge/python-3.10-3776AB?logo=python&logoColor=white)](https://www.python.org) [![License](https://img.shields.io/badge/license-Apache--2.0-blue.svg)](LICENSE)

제품별 온라인 채널 판매량을 예측한 LG Aimers 3기 연계 데이터 해커톤 기록입니다. 판매 이력을 시계열 학습 테이블로 바꾸고 재귀적으로 다음 구간을 예측해 예선 상위 1.6%로 본선에 진출했습니다.

## 개요

| 구분 | 내용 |
| --- | --- |
| 대회 | 온라인 채널 제품 판매량 예측 AI 온라인 해커톤 |
| 기간 | 2023.08.01 – 2023.08.28 |
| 주최 / 주관 | LG AI Research / 데이콘 (참여: 한경닷컴) |
| 평가지표 | Pseudo SFA (PSFA) |
| 결과 | 예선 상위 1.6% (본선 진출) |
| 과제 | 제품별 온라인 채널 판매량 시계열 예측 |
| 연계 활동 | LG Aimers 3기 |

## 접근

- wide 형식 판매 이력을 제품별 long 시계열 학습 테이블로 변환했습니다.
- lag, 이동 통계, 달력 주기, 제품 메타데이터 피처를 만들었습니다.
- log 변환한 타겟으로 tabular 회귀 모델을 학습했습니다.
- 재귀적 multi-step 예측으로 제출 구간을 채웠습니다.

## 저장소 구성

```text
.
├── notebooks/
│   ├── 01_data_overview.ipynb
│   └── 02_forecasting_pipeline.ipynb
└── requirements.txt
```

## 공개 범위

대회 원본 데이터, 모델 파일, 제출 파일은 포함하지 않았습니다. 데이터는 대회 참가자에게만 제공되어 그대로 재현하기는 어렵고, 저장소에는 접근 방식을 담은 노트북만 남겼습니다.

## 링크

- [대회 페이지](https://dacon.io/competitions/official/236129/overview/description)
- [최종 리더보드](https://dacon.io/competitions/official/236129/leaderboard)

## 라이선스

Apache License 2.0. 자세한 내용은 [LICENSE](LICENSE)에 있습니다.
