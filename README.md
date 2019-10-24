# Batch Pipeline 튜토리얼


  ## 튜토리얼 내용

   > 집 값을 예측하기 위한 ML 모델을 만들기 위해  House Prices 데이터를 BatchPipeline 서비스를 활용해 전처리 하고 HDFS에 저장한다.

  ## 튜토리얼 데이터

   * [train.csv](https://www.kaggle.com/c/house-prices-advanced-regression-techniques/download/train.csv)

    81개의 컬럼 중 10개의 컬럼을 사용할 예정

   | 컬럼 명      | 내 용 |
   | ------------ | ----- |
   | Id           | 집의 고유번호  |
   | SalePrice    | 판매가격      |
   | YearBuilt    | 지어진 년도      |
   | 1stFlrSF     | 1층 면적      |
   | 2ndFlrSF     | 2층 면적      |
   | GarageCars   | 차고 면적      |
   | PoolArea     | 수영장 면적      |
   | Street       | 집 앞 거리 포장 유형      |
   | Neighborhood | 지역      |
   | KitchenQual |  주방 상태     |
  
  ## 데이터 전처리 시나리오
     1. importHDFS노드를 활용해 HDFS에서 데이터를 불러온다.
     2. filter 노드를 활용해 Outliers를 제거한다.
     3. fillna 노드를 활용해 null 데이터를 채워넣는다.
     4. select 노드를 활용해 원하는 컬럼을 선택한다.
     5. replace 노드를 활용해 문자를 치환한다.
     6. cast 노드를 활용해 특정 컬럼의 데이터 타입을 변경한다.
     7. withColumn 노드를 활용해 새로운 컬럼을 만든다.

  ## Modeling data 생성
  
  
