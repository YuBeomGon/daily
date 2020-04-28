Pet 2nd Meeting
=============
Contents
-------------
#### 진단코드 분류
#### 처치용어 클러스터링
#### Bert / Albert 소개

* * *

### 진단코드 분류
1. setup
* 총 class 50개(진단코드당 최소 50개 이상)
* labeld data 약 16000개 중 약 8000개, 약 &:2:1의 비율로 train, dev, test set
* unlabeled data 약 30만 개
* 

2. Bert
* 사전학습된 bert(multi-lingual model) 모델 + fine tunning(labeled data) : 약 60% accuracy 
* 사전학습된 bert(multi-lingual model) 모델 + pretraing with (unlabeled data) + fine tunning(labeled data) : 약 5% 성능 상승

3. Albert(a lite bert)
* pretraing with (unlabeled data) + fine tunning(labeled data) : 약 95~99% accuracy
* fine tunning(labeled data) : 
* Bert에 비해 shared unit을 사용한 albert model이 domain specific한 data의 context를 잘 잡아내는 것으로 보임,
* 일반화 
  * more data
  
* * *
  
### 처치 용어 클러스터링

1. setup
* 총 12만 개의 data( 중복 제외시 6만개의 처치 관련 용어)
* 희소 데이터 제거 및 중복데이터 개수 최소화, 총 8900여개
* Bert multi-lingual을 이용 처치 용어 벡터화
* K means clustering 이용하여 50개의 class로 clustering(약 10시간 소요)
* 두번 세번 반복 후 majority vote방식

* * *

### Bert / Albert 소개

