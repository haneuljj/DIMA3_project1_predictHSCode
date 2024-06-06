# 🔢 HS Code 추천 시스템 개발 🔢

![python](https://img.shields.io/badge/Python-14354C?style=for-the-badge&logo=python&logoColor=white)
![jupyeter](	https://img.shields.io/badge/Made%20with-Jupyter-orange?style=for-the-badge&logo=Jupyter)

## 🖇️ 프로젝트 기획
- HS 코드 선정은 수출입 과정에서 관세 설정에 영향을 미치므로 매우 중요한 과정이지만 일반 중소기업들은 수출입 상품의 HS 코드를 선정하는 데 어려움을 겪는 경우가 존재
- 상품설명만으로 HS 코드를 예측할 수 있도록 하여 HS코드 선정 과정 간소화
- 머신러닝, 딥러닝 및 코사인 유사도를 함께 활용하여 입력값에 대한 HS 코드 예측의 정확도를 높일 수 있는 텍스트 분류 모델 구현 목표

## 🧑‍🤝‍🧑 개발 기간 / 인원
2023.12~2024.01(5주) / 6명

## 🛠️ 개발도구
- 언어: Python 3.11
- 개발환경: Anaconda Jupyter Notebook
- 라이브러리: selenium, pandas, numpy, nltk, scikit-learn, tensorflow, googletrans API

## ✏️ 프로젝트 과정
### 1. 데이터 수집
- 관세법령정보포털 사이트에서 약 10년 기간에 해당하는 12만여개의 HS코드 결정 사례와 HS코드 해설서 정보 수집
- 대량의 정보를 수집하기 위해 파이썬으로 자동 크롤링 코드 구현

### 2. 데이터 전처리
1) 국내 사례는 googletrans api로 영어 번역
2) 중복행 제거
3) HS코드(y값) 형식 통일
4) 소문자변환
5) 구두점 및 불용어 제거
6) 품사 태깅 및 표제어 추출
7) TF-IDF Vectorizer를 통한 자연어 벡터화
 
### 3. 모델링
- 적합한 분류 모델을 찾기 위해 Logistic Regression, RandomForestClassifier, LSVC 모델 학습 및 평가
- 평가 점수가 높은 LSVC 채택
- 모델의 성능 개선을 위해 LSTM 모델 개발 및 HS코드의 주요 키워드를 학습한 코사인 유사도 모델 개발
- 세 모델을 합친 앙상블 모델 개발
<img src="https://github.com/haneuljj/DIMA3_project1_predictHSCode/assets/146147196/54030996-0214-4fd4-bb28-360aa1cf3f2b.png" width="680" height="300"/> 

## 🗝️ 프로젝트 결과
<img src="https://github.com/haneuljj/DIMA3_project1_predictHSCode/assets/146147196/39ec16cd-6ec1-48b9-8762-04f67f55e11a.png" width="680" height="400"/> 



