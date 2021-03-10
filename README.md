# ISEOULKIUM

## 주제
돌봄수요에 기반한 우리동네키움센터 최적입지 추천

## 개요
맞벌이부부가 늘어나면서 아이 돌봄 서비스의 수요는 계속해서 증가하고 있지만, 2019년 기준, 한국 초등학생 공적 돌봄 서비스 비율은 13.9퍼센트로 OECD 평균의 절반에도 미치지 못합니다.  절대적인 수의 부족과 더불어 기존 연구들에서 지적한 수요에 따른 공급을 실현하기 위해, 틈새공백이 많이 발생하는 지역을 추정하고 '우리동네키움센터'의 최적위치를 추천하는 방법을 모색하엿습니다.

## 분석배경 
**우리동네 키움센터는 서울시 어느 장소에 우선적으로 설치되어야 할까? 
**![image](https://user-images.githubusercontent.com/67999107/110648472-1771ae80-81fc-11eb-98b0-7611ae18fd87.png)

현재 구별로 불균형하게 입지되어 있는 것의 이유를 살펴보고, 우리동네키움센터의 운영방향과 정체성에 맞는 위치를 찾으려 노력하였습니다. 

** 분석방향 ** 
우리동네 키움센터 설립 취지에 맞게

1. 돌봄의 사각지대에 놓인 초등학생들이 많고
2. 돌봄의 인프라가 부족한 지역 중
3. 공적 돌봄시설에 대한 선호도가 높은 지역(소득분위고려)에

우선적으로 '우리동네키움센터'가 입지할 수 있는 모델을 만들자 
![image](https://user-images.githubusercontent.com/67999107/110649025-936bf680-81fc-11eb-81fd-c8216ae82226.png)

## 분석방법
1. '우리동네키움센터' 최적입지 산출과정 

![image](https://user-images.githubusercontent.com/67999107/110649169-b4344c00-81fc-11eb-8ec3-b88f941ff2f7.png)

  (1) 돌봄 틈새공백인구 추정
  - 돌봄틈새공백: 집에 도착한 초등학생이 부모의 보살핌을 받기까지 기존의 공적 돌봄 프로그램으로 메꾸기 힘든 시간적 틈새
- 추정 방식: 맞벌이 부모 슬하 초등학생 중, 7시 이전에 집에 혼자 있는 인구
    →  돌봄의 사각지대에 있는 초등학생 인구
  ![image](https://user-images.githubusercontent.com/67999107/110649411-e80f7180-81fc-11eb-80f5-ed7002f6531b.png)
  
  (2) 돌봄인프라 지수
  ![image](https://user-images.githubusercontent.com/67999107/110649503-ff4e5f00-81fc-11eb-8cfa-474e456be204.png)
  ![image](https://user-images.githubusercontent.com/67999107/110649531-070e0380-81fd-11eb-8c9b-1546044c6980.png)
  
  (3) 공적돌봄시설 선호도 (소득분위) 
  - 소득에 따라 공적돌봄시설 및 사설 교육기관에 대한 수요가 다름. 
  - 따라서 **공적돌봄시설**에 대한 수요가 높은 곳에 우선 배치를 하기 위해 지역 소득을 고려
  - KNN regressor를 활용한 지역소득 추정
  ![image](https://user-images.githubusercontent.com/67999107/110649774-450b2780-81fd-11eb-8dd1-b851b453b390.png)

(4) 선형결합을 통한 행정동 별 돌봄수요 지수 산출
![image](https://user-images.githubusercontent.com/67999107/110649896-64a25000-81fd-11eb-9766-e21fe893f872.png)
![image](https://user-images.githubusercontent.com/67999107/110650122-9adfcf80-81fd-11eb-98f3-d877c12fee4f.png)

(5) 각 행정동 내 250mx250m 격자를 기준으로 수요 지수 산출 

## 결과
![image](https://user-images.githubusercontent.com/67999107/110650228-b4811700-81fd-11eb-88cb-784d4d60aec0.png)

1. 공급 미달량 상위 3개동 최적입지 격자 선정
![image](https://user-images.githubusercontent.com/67999107/110650475-ebefc380-81fd-11eb-94de-62d8de28ffce.png)


2. 프로젝트 기준 날짜 이후에 신설된 시설의 예약률과 최적입지 모델링 결과 비교
![image](https://user-images.githubusercontent.com/67999107/110650499-f316d180-81fd-11eb-940b-3f64252c4cd5.png)
-> 예약률이 상위인 곳은 최적입지 결과와 가까운 격자에 입지해있음을 확인할 수 있습니다. 

