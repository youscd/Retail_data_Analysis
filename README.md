## Retail_data_Analysis (personal project)
* data source : kaggle
* os : Ubuntu 22.04, Windows 10
* python version : 3.10.12, 3.12.1

---

## 분석 시각화
### # Customer_Segment(소비등급) 컬럼의 값을 기준으로 분석 및 시각화
- 연도별, 월별 매출 비교
- 소비등급과 소득수준의 관계
- 소비등급별 나이, 성별 매출 비교
- 소비등급별 평점과 피드백
- 소비등급별 국가별, 지역별 매출 비교
- 소비등급별 상품별 매출

![image](https://github.com/user-attachments/assets/76ff805d-366d-4e4c-a57e-1c64cb34eb2d)

---

### # 새 컬럼 생성
#### 1. Age_Group(연령대) 컬럼
- 10대 ~ 70대 값으로 Age(나이) 컬럼의 값을 범주화

#### 2. Time_Group(시간대) 컬럼
- 구매시간 값을 기준으로 오전, 오후를 구분하는 컬럼 생성
- Time(시간) 컬럼(%H:%M:%S 형태) 에서 시간(hour) 값만 가져와 Hour(시) 컬럼 생성
- Hour(시) 컬럼 값을 기준으로 오전 / 오후 를 구분하는 Time_Group(시간대) 컬럼 생성

#### 3. Month(월) 컬럼
- Regular 등급 고객들의 월별 구매 패턴을 파악하기 위해 Month(월) 컬럼을 기준으로 데이터 정렬
- Date(구매날짜) 컬럼의 값과 Month(월) 컬럼의 값이 맞지 않는 것을 발견
  예) Date(구매날짜) 값 : 8/25/2023 , Month(월) 값 : February
- Date(구매날짜) 컬럼의 값을 기준으로 Month(월) 컬럼 재 생성

---

## 분석 시각화 모듈화
### # 데이터 오류 발견
- Month(월) 칼럼을 새로 생성한 후 데이터를 살펴본 결과,\
  2년 간의 데이터가 아닌 1년 간(23.03 ~ 24.02)의 데이터임을 확인

### # 모듈화하여 다른 등급의 매출 시각화
- 주요 시각화 코드를 모듈화
- Premium, New 등급 고객들의 매출을 시각화하여 확인

---

## 분석 결과
- 각 등급별 구매 패턴이 비슷하게 나타남

### 1) 연도별, 월별 매출 비교
- 23.03 ~ 24.02 기간 동안 모든 등급의 월별 매출에 큰 변동이 없었음

![image](https://github.com/user-attachments/assets/dddbc3ea-b8b5-4c7e-877a-d41b53fb4820)

### 2) 소비등급과 소득수준의 관계
- 세 소비등급(Premium, Regular, New) 중에서 Regular 등급의 소비가 가장 많음
- 소득수준이 medium 이고 Regular 등급인 고객이 가장 구매를 많이 함

### 3) 소비등급별 나이, 성별 매출 비교
- Premium 등급은 40대의 구매가, Regular, New 등급은 20대의 구매가 가장 많음
- 모든 등급의 남성 고객이 여성 고객보다 구매금액이 1.5배 높음

![image](https://github.com/user-attachments/assets/3f721094-69d3-41f7-979d-04d8ac04b46e)

### 4) 소비등급별 평점과 피드백
- 모든 등급이 평점의 경우 4.0점, 피드백의 경우 Excellent, Good 으로 준 경우가 많았음

### 5) 소비등급별 국가별, 지역별 매출 비교
- 모든 등급이 'Germany', 'Australia', 'UK', 'Canada', 'USA' 5개의 나라 중\
USA의 매출이 가장 많았으며, 나머지 나라는 비슷한 비율을 가짐
- 각 등급에 따라 USA 의 경우 지역별로 구매금액에 약간의 차이 존재

### 6) 소비등급별 상품별 매출
- 모든 등급이 식료품과 전자제품의 구매가 가장 많음
  (이외에 의류, 도서, 잡화 등은 비슷)
- New 등급의 경우 식료품보다 전자제품의 구매가 더 많음
- 모든 등급들의 가장 구매가 많았던 브랜드는 Pepsi
