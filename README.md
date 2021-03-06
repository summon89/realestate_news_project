## realestate_news_project
부동산 뉴스 데이터를 활용한 부동산 정보 제공(비정형, NLP)
- 프로젝트 목표 : 부동산뉴스를 분류·정제하여 아파트매매가격과의 연관성 분석 및 가격예측,토픽별 주요 뉴스및 키워드 등 <br>
소비자에게도움될수있는비정형부동산정보를제공한다.



## 데이터 수집
- 빅카인즈 OPEN API
- KB부동산 아파트매매가격지수
- 아파트실거래가상세조회 OPEN API

## 감성지수
- 뉴스 제목(title) OKT 형태소 분석기 사용
- 비지도학습 : 1차 부동산 도메인 직접 긍부정 라벨링, 2차 군산대 감성사전 사용

## 벡터화
- TF / TF-IDF Vectorization

## 연관분석
- K-means, 토픽모델링(LDA) 방식

## 주요 뉴스 및 키워드
- TEXTRANK 사용

## 부동산 가격 예측
- 입력변수 : 200개 군집의 Centroid와 TF-IDF 벡터 간 유사도 거리 + 감성지수 => 총 201개 차원
- 종속변수 : 주간 아파트매매가격지수(KB부동산)
- 모델링 : 단일모델 적용(Linear, xgb, ada 등)
