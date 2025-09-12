## Team6 - 🏠 서울 아파트 매매 실거래가 예측 경진대회

<table>
  <tr>
    <td> <div align=center> 👑 </div> </td>
    <td> <div align=center> 🧔 </div> </td>
    <td> <div align=center> 🌹 </div> </td>
    <td> <div align=center> 👨🏻‍🎓 </div> </td>
    <td> <div align=center> ✏️ </div> </td>
  </tr>
  <tr>
    <td> <div align=center> <b>임환석</b> </div> </td>
    <td> <div align=center> <b>김종범</b> </div> </td>
    <td> <div align=center> <b>윤소영</b> </div> </td>
    <td> <div align=center> <b>권효주</b> </div> </td>
    <td> <div align=center> <b>최현</b> </div> </td>
  </tr>
  <tr>
    <td> <img alt="Github" src ="https://png.pngtree.com/thumb_back/fh260/background/20230613/pngtree-the-high-man-jesus-is-standing-up-among-the-clouds-image_2974129.jpg" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="https://avatars.githubusercontent.com/u/39229081?v=4" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="https://ca.slack-edge.com/T095CFN0ZT6-U096YNDM3CZ-94526243865c-512" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="https://ca.slack-edge.com/T095CFN0ZT6-U0960JE97NW-fd9ca66411f0-512" width="250" height="300"/> </td>
     <td> <img alt="Github" src ="https://avatars.githubusercontent.com/u/220303245?v=4" width="250" height="300"/> </td>
  </tr>
  <tr>
    <td> <div align=center> <a href="https://github.com/hwan-han"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href="https://github.com/kirin72"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href="https://github.com/yourhotb"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href="https://github.com/hopeplanting"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
     <td> <div align=center> <a href="https://github.com/yagopji"> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    </tr>
</table>

---
       
## 1. 🏆 대회 소개

* <b>주제</b> - 서울 아파트 매매 실거래가 예측 (Regression)

* <b>평가지표</b> - RMSE (예측값과 실제값 간 평균 편차)

* <b>기간</b> - 2025/9/1(월) ~ 9/11(목)

* <b>규정 핵심</b>
  * 외부 데이터 허용 (단, 평가 데이터 유추 금지)
  * 평가 데이터 학습 금지
  * 사전학습 가중치 금지 (토크나이저는 허용)
  * 팀당 일일 제출 12회
<br></br>
## 2. 📅 대회 일정
| 날짜 | 내용 |
|:---|:---|
| 08.18 | 팀 결성 |
| 09.01 | OT, 팀원 추가 (권효주 님 합류) |
| 09.01 ~ 09.05 | ML Advanced + Regression 실습 |
| 09.05 | ML 라이브 세션 (이가람 멘토님) |
| 09.08 ~ 09.11 | 경진대회 집중 기간 |
| 09.12 | 경진대회 발표 |

## 3. 🎯 목표

- **대회 공식 목표** - RMSE 최소화 (리더보드 기준)
- **우리 팀 목표** - 성능 경쟁보다 **학습·지식 공유**에 중점
    - 각자 전처리·모델링 실습 → 팀 내 설명/공유
    - 외부 데이터 탐색 & 아이디어 확장
    - 서로 다른 접근법 비교를 통한 학습 극대화

## 4. ⚙️ 환경 세팅

```
# Python 3.10 권장
# 필요한 라이브러리 설치
pip install pandas numpy scikit-learn lightgbm eli5 haversine optuna xgboost joblib matplotlib seaborn tqdm

# NanumGothic 폰트 설치
sudo apt-get install -y fonts-nanum
```
## 5. 📂 폴더 구조
```
├── baseline_code
│   ├── baseline_code.ipynb        # 베이스라인 코드
│   └── requirements.txt           
├── data                           # 대회 제공 원본 데이터 공간
│   ├── bus_feature.csv            
│   ├── subway_feature.csv
│   ├── train.csv                
│   ├── test.csv
    └── sample_submission.csv      # 제출 양식 예시                
├── notebooks                      # 개별 작업 공간
├── src                            # 전처리/모델링 작업 공간                  
├── output                         # 산물 저장 공간                
└── README.md                      

```
## 6. 💽 데이터 개요

#### **6-1. 대회 제공 파일**

- **`train.csv`**
- **`test.csv`**
- **`bus_feature.csv`** - 버스 정류장/노선 피처
- **`subway_feature.csv`** - 지하철역/노선 피처
- **`sample_submission.csv`** - 제출 양식

#### **6-2. 전처리 산출물**
- **`merge_subway_fixed.csv`** - 원본 데이터를 결합하고 결측/파생을 반영한 **최종 학습 입력 데이터**

#### 6-3. 데이터 파이프라인
```
train.csv + test.csv
  + bus_feature.csv + subway_feature.csv
  └─▶ [좌표 보정, 결측 대체, 피처 결합/생성] ─▶ merge_subway_fixed.csv
```

## 7. 🔎 EDA
- **결측치 확인** - matplotlib을 활용해 변수별 결측치 비율 시각화
- **변수 상관관계 분석** - 히트맵을 이용해 변수들 간 상관관계 파악
- **정규화 적용** - 변수 중요도 비교 시 정규화로 상대적 영향력 확인

## 8. 🧹 데이터 전처리
  ### 8-1. 기본 전처리
  - **컬럼 정리**
    - 불필요한 열 및 결측치가 10만 개 이상인 컬럼 삭제
    - 컬럼명 표준화 (전용면적(㎡) → 전용면적, X/Y좌표 → 좌표X/Y)
  - **위치 정보 정제**  
    - 카카오 API를 활용해 아파트명 + 주소 매칭해 좌표 결측치 보완
    - API DB 특성상 2015년 이후 주소 데이터만 안정적 제공
    - 매핑으로 채우지 못한 0.4%는 시군구 평균·중앙값으로 대체
  
  ### 8-2. 외부 데이터 병합
  - **금융 데이터 (ecos, 한국은행 경제통계시스템)**  
    - 한국은행기준금리, 정부대출금리, 국고채(3년), 서울지가변동률 추가  
    - 계약년월 기준으로 매핑  
    - 단기 상관관계는 낮으나, 금리는 1~2년 후 영향  
    - 변수들 간 상관관계가 높아 일부는 통합 처리 가능  
  - **지하철 데이터 (subway_feature.csv)**  
    - 좌표 기반 매핑  
    - 주요 변수: `1km내역개수`, `가까운역이름`, `실제 거리`
      
  ### 8-3. 파생변수 생성
  - Haversine 공식 → 1km내 역 개수, 지하철/버스 정류장 거리 계산  
  - `전용면적(㎡)` → `전용면적` 표준화  
  - `계약년월` → `계약년`, `계약월` 분리  
  - 2020년 이후 건축 → `신축여부` 플래그  
  - 강남·서초·송파·용산 → 특이 지역 플래그  
  - 전용면적 구간화 - 25%, 50%, 75% 분위수 기준으로 나눠 구간별 평균값 반영

  ### 8-4. 중요 피처
  - **전용면적** - Target값과 대체로 비례
  - **아파트명** - 지역·브랜드 효과를 반영, 범주형 처리 시 모델 주요 분할 기준으로 작용  
  - **가까운역** - 교통 접근성을 반영, 거리·역 이름 변수 모두 가격에 직접적 영향  
  - **국고채** - 단기 상관관계는 낮지만, 중장기 가격 흐름에 변수로 작용
  - 일부 이상치(outlier) 존재 → log 변환으로 분산 축소  
  - 구간화 - 25%, 50%, 75% 분위수 기준으로 나눠 구간별 평균값 학습에 반영
  
  ### 8-5. 타깃 변환
  - `target`에 log1p 변환 적용 후 학습  
  - 제출 단계에서 expm1 역변환 수행  
  - 분포 안정화 및 RMSE 계산 안정성 강화

## 9. 🤖 모델링

- **모델 선택**  
  - LightGBM Regressor 사용  
  - XGBoost와 함께 대표적인 경량화 부스팅 모델  
  - 빠른 학습 속도 + 우수한 예측 성능 → 대용량 데이터셋에도 효과적  

- **교차 검증**  
  - 시계열 데이터 특성을 반영 → `TimeSeriesSplit(n_splits=5)` 적용  
  - 미래 시점 예측 목적에 부합하는 검증 방식  

- **카테고리 처리**  
  - object 타입 변수를 category로 변환  
  - LightGBM이 범주형 변수를 효율적으로 처리할 수 있게 최적화  

- **하이퍼파라미터**  
  - `n_estimators=5000`, `learning_rate=0.05`, `subsample=0.8`, `colsample_bytree=0.8`  
  - `early_stopping_rounds=50` → 과적합 방지 목적  

- **타깃 변환**  
  - target → log1p 변환 후 학습 → 예측값은 expm1로 역변환  
  - 왜곡된 분포 완화, 학습 안정성 및 RMSE 계산 안정화  

- **추론 및 앙상블**  
  - 각 fold별 모델을 `timeseries_fold{k}_gbm.pkl`로 저장  
  - 최종 예측 시 fold별 결과를 평균 앙상블하여 일반화 성능 강화  

- **Feature Importance 결과**  
  - 전용면적, 아파트명, 교통 변수, 금융 지표 등이 중요 요인으로 확인됨  
  - 특히 금리 지표는 단기 영향은 낮으나 중장기 가격 흐름에 의미 있는 피처로 작용  

## 10. 📊 결과
**Public Leaderboard RMSE** - 15514.1856
<br></br>
## 11. 📚 참고

- **데이터 출처**
  - [서울시 공공주택 아파트 정보 (CC BY)](https://data.seoul.go.kr/dataList/OA-15818/S/1/datasetView.do)  
  - [국토교통부 실거래가 (정부 3.0 / 공공데이터 개방)](https://rt.molit.go.kr/pre.html)  

- **참고 문헌**
  - *딥러닝과 머신러닝을 이용한 아파트 실거래가 예측*  
    (*Apartment Price Prediction Using Deep Learning and Machine Learning*)  
    김학현, 유환규, 오하영.  
    한국정보처리학회 소프트웨어 및 데이터 공학 논문지, 제12권 2호, pp. 59–76, 2023.  
    [DOI: 10.3745/KTSDE.2023.12.2.59](https://doi.org/10.3745/KTSDE.2023.12.2.59)

- **라이브러리/도구**
  - [LightGBM Documentation](https://lightgbm.readthedocs.io/)  
  - [Optuna Documentation](https://optuna.org/)  
  - [카카오 주소/좌표 API](https://developers.kakao.com/docs/latest/ko/local/dev-guide)  
