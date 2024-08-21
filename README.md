## Retail_data_Analysis (personal project)
* data source : kaggle
* os : Ubuntu 22.04, Windows 10
* python version : 3.10.12, 3.12.1

---

## 분석 시각화
### 2023년에서 2024년, 2년 간의 고객 구매 데이터

![image](https://github.com/user-attachments/assets/76ff805d-366d-4e4c-a57e-1c64cb34eb2d)

#### 1. 년도별, 월별 매출 비교
- 2024년에 비해 2023년도 매출액이 월등히 높음
- 2년 동안 가장 구매금액이 많은 소비등급은 Regular 등급
- 2년 동안 가장 매출이 많았던 달은 4월 (다음으로 8월, 5월 순)
- Regular 등급은 7월, 4월, 1월 순 (다른 소비등급에 비해 7월의 구매금액이 가장 많음)
- 전체적으로 2023년도의 매출에 비해 2024년의 매출이 현저히 낮지만,\
  2024년 1 ~ 2월의 매출은 전년도에 비해 월등히 높음

#### 2. 소비등급과 소득수준의 관계
- 소득수준이 medium 이고 Regular 등급인 고객이 가장 구매를 많이 함

#### 3. Regular 등급의 나이, 성별 매출 비교
- 전 연령대에서는 20대의 구매가 가장 많았으며,\
  남성의 구매 정도가 여성의 2배 수준으로 더 많음

#### 4. Regular 등급의 평점과 피드백
- 대부분이 높은 평점과 좋은 피드백을 많이 준 것으로 보아 구매에 만족했다 볼 수 있음

#### 5. Regular 등급의 국가별, 지역별 매출 비교
- 'Germany', 'Australia', 'UK', 'Canada', 'USA' 5개의 나라 중\
USA, UK, Germany 순으로 많았으며, USA 의 경우 지역별로 구매금액에 차이 존재

#### 6. 상품별 매출
- 전자제품의 구매가 가장 높았고, 다음으로 식료품
  (이외에 의류, 도서, 잡화 등은 비슷)
- 가장 구매가 많았던 브랜드는 Pepsi

---

## 소비등급평가
이미 부여된 소비등급이 어떤 기준으로 부여되었던 것인지 확인해보기 위해 군집화 및 분류예측 수행 예정
