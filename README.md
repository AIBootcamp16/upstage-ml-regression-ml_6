# House Price Prediction | 아파트 실거래가 예측
## Team

<table>
  <tr>
    <td> <div align=center> 👑 </div> </td>
    <td> <div align=center>  1 </div> </td>
    <td> <div align=center>  2 </div> </td>
    <td> <div align=center>  3 </div> </td>
    <td> <div align=center>  4 </div> </td>
  </tr>
  <tr>
    <td> <div align=center> <b>최현</b> </div> </td>
    <td> <div align=center> <b>임환석</b> </div> </td>
    <td> <div align=center> <b>김종범</b> </div> </td>
    <td> <div align=center> <b>윤소영</b> </div> </td>
    <td> <div align=center> <b>권효주</b> </div> </td>
  </tr>
  <tr>
    <td> <img alt="Github" src ="" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="" width="250" height="300"/> </td>
    <td> <img alt="Github" src ="" width="250" height="300"/> </td>
  </tr>
  <tr>
    <td> <div align=center> <a href=""> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href=""> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href=""> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href=""> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    <td> <div align=center> <a href=""> <img alt="Github" src ="https://img.shields.io/badge/Github-181717.svg?&style=plastic&logo=Github&logoColor=white"/> </div> </td>
    </tr>
</table>
## 0. 개요
### 서울시의 집 값 예측 프로젝트

### Requirements

각자 역할을 분담해서 작업

## 1. Competiton Info

### Task

* 데이터 확인 및 수집
* 데이터 전처리 및 EDA
* 모델링
* 파라미터 수정
* 결과 정리

### Timeline

- 9/1 ~ 9/3 이론 공부
- 9/4 첫 미팅 후 환경 작업 환경 세팅
- 9/5 두번째 미팅
- 9/7 세번째 미팅
- 
## 2. Components

### Directory

- _Insert your directory structure_

File Tree
```
├── data
│   ├── test.csv
│   └── train.csv
├── notebooks 
│   
└── output

```

## 3. Data descrption

### Dataset overview

1. 주어진 버스정류장과 지하철역과의 거리를 아파트와 합치기 위해서 필요한
아파트의 X,Y좌표 결측치가 80만개정도로 많습니다.
2. 머신러닝에 필요없는 열이 많습니다.


### EDA

1. 너무 필요없는 열이 많고 결측치도 많습니다.
2. 히트맵으로 각 변수들의 상관관계를 보고 중요한 열을 체크합니다.
3. 데이터 결측치가 100만이 넘는것들을 체크합니다.
4. metplotblib을 활용하여 결측치가 많은 순서를 그래프로 보면서 히트맵으로 확인한 중요도를 별도로 체크하였습니다.

### Data Processing

1. 거래에 필요없는 열을 드롭합니다.
2. 결측치를 채웁니다. (XY좌표,외 수치열, 범주형은 아파트이름은 도로명으로 나머지는 없음으로)
3. XY좌표 정제(서울범위를 벗어난 좌표는 중앙값으로 채움)
4. 2020년부터 지어진 아파트는 신축으로 신축여부 추가
5. 강남,서초,송파,용산의 특이한 지역은 별도 표기하는 열 추가
6. 지하철데이터 좌표,중복정제하여 가까운 역과 거리 열 추가
7. 버스데이터 좌표,중복정제하여 가까운 정류장과 거리 열 추가
8. 한국은행금리,국고채,정부대출금리,서울지가변동율 추가
9. 초등학교,중학교,고등학교 거리 추가
10. 이후 결측치를 모두 채우기 위해 수동으로 작업
11. 머신러닝에 적당한 데이터로 가공(년도 날짜를 기준으로 행을 줄이는 등)

## 4. Modeling

### Model descrition

- _Write model information and why your select this model_

### Modeling Process

- _Write model train and test process with capture_

## 5. Result

### Leader Board

- _Insert Leader Board Capture_
- _Write rank and score_

### Presentation

- _Insert your presentaion file(pdf) link_

## etc

### Meeting Log

- _Insert your meeting log link like Notion or Google Docs_

### Reference

- _Insert related reference_
