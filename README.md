# RFM 고객세분화를 통한 고객별 추천시스템

## 프로젝트 개요
### 1. 기획의도
  -  고객별로 성향과 특징이 다 다르기 떄문에 일괄적인 추천시스템을 적용할 수는 없다.
따라서 여러 기준을 설정하여 고객을 분류한 후 해당 고객에 각각 다른 모델을 적용하도록 프로젝트를 진행하였다.
### 2. 기대효과
  -  실제 기업에서 사용하는 RFM을 이용한 고객별 추천시스템을 간접적으로 체험할 수 있다.
  -  추천시스템과 관련된 다양한 모델들을 공부할 수 있다.
<br/>

## 프로젝트 구조
### 1. 프로젝트 진행과정

|날짜|세부 내용|
|:------:|---|
|2/1 - 2/3|데이터 탐색 및 CB 모델 구축|
|2/4|1차 중간점검|
|2/5 - 2/6|RFM 생성 및 NLP 모델 학습|
|2/7|2차 중간점검|
|2/8 - 2/10|ALS 모델링 및 평가지표|
|2/13 - 2/14|프로그램 테스트 및 모듈화|
<br/>

### 2. 데이터셋 및 파이프라인
  - 데이터는 캐글에 있는 fashion campus 데이터 활용<br>
     <https://www.kaggle.com/datasets/latifahhukma/fashion-campus><br/><br/>
  -   파이프라인
<img src="https://github.com/hwyoon217/recommend_model_project/blob/main/pipeline.PNG" width="1400" height="600"/><br/><br/>

### 3. 결과<br/>
<img src="https://github.com/hwyoon217/recommend_model_project/blob/main/result.PNG" width="1400" height="400"/><br/>
  -  RFM을 통해 세분화된 고객들에게 각각 다른 모델을 적용하여 상품을 추천
  -  CB 모델의 경우 precision@k 값이 0.2, recall@k 값이 0에 수렴하는 값이 나옴.
  -  ALS 모델의 경우 하이퍼파라미터 튜닝 결과 factors: 50, iteration : 10, regularization: 0.001 일 때 성능이 가장 좋음
  <br/>

## 회고
  -  EDA 결과, 매년 모바일 이용자 수가 꾸준히 증가하는 것을 알 수 있다. 따라서 모바일 이용자만 따로 추출하여 추천시스템을 구축할 예정이다.
  -  RFM을 3개 기준(구매가격, 최근구매일, 구매빈도)로 나누어 진행했는데 기준을 다르게 설정한다면 성능이 어떻게 나올지 궁금하다.
