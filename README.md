# recommend_model_project

## 프로젝트 개요
1. 기획의도
  -  다양한 분야에서 추천시스템이 쓰이고 있기 때문에 이러한 추천시스템을 이해하고 직접 구현해보고자 이번 프로젝트를 실행

2. 기대효과
  -  추천시스템에 대한 이해와 추천시스템 구축
  -  추천시스템과 관련된 다양한 모델들을 공부
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
  -  NLP 모델의 경우 precision@k 값이 0.2, recall@k 갑시 0에 수렴하는 값이 나와서 성능면에서는 많이 아쉬움
  -  ALS 모델의 경우 하이퍼파라미터 튜닝 결과 factors: 50, iteration : 10, regularization: 0.001 일 때 성능이 가장 좋음
  <br/>

## 회고
  -  NLP 모델의 경우, 평가지표가 생각보다 낮게 나온것과, recall@k 값을 올리지 못한 것이 너무 아쉬웠다.
  -  EDA 결과, 매년 모바일 이용자 수가 꾸준히 증가하는 것을 알 수 있다. 따라서 모바일 이용자만 따로 추출하여 추천시스템을 구축할 예정이다.
