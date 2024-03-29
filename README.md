# 2021년 11월 민원 데이터 분석 공모전 #

장려상(동국대학교 통계학과)

#1

![슬라이드2](https://user-images.githubusercontent.com/75729975/207486082-2a0d7799-ad34-4bb7-978a-48b1692816d4.PNG)

민원 데이터에 대한 자유 분석이 주제였으며, 세부 주제로는 민원 데이터를 활용하여, 이미 제안된 민원과 유사한 정도를 텍스트마이닝을 통해 측정하여 민원 관리자와 민원인 양 쪽에서 시간을 단축하고 노동력을 절감할 수 있도록 하였다. 해당 분석을 실제로 활용하기 위하여, Python을 통해 간단한 검색 시스템까지 구현하고자 하였다.



#2

![슬라이드3](https://user-images.githubusercontent.com/75729975/207486084-076371ca-ebca-402d-8beb-c7360aa87b1c.PNG)

프로젝트의 흐름을 도식화함.



#3

![슬라이드4](https://user-images.githubusercontent.com/75729975/207486087-15a08032-363b-4d5d-9508-6226e7186699.PNG)

주 분석 방법으로는 LDA 토픽모델링을 활용하였다. 토픽모델링을 통해 텍스트 데이터를 클러스터링 비슷하게 하였다.



#4

![슬라이드5](https://user-images.githubusercontent.com/75729975/207486097-030a4a20-84fb-481c-9320-2c8dfb815b25.PNG)

Tf-idf를 이용해서 임베딩 처리한 텍스트 데이터를 통해, 유사도가 높은 과거의 민원을 뽑아오고, 그 과정에서 Filtering을 해주는 방법론으로 이전 슬라이드의 토픽 모델링을 활용한 토픽 index을 활용하였다. 즉, 토픽이 동일한 민원 내에서 유사도가 높은 것을 긁어온다.



#5

![슬라이드6](https://user-images.githubusercontent.com/75729975/207486104-bd9ed06a-5fcc-4cc5-b45e-8e659f6dd606.PNG)

Python Flask를 활용하여 검색 서비스를 간단하게 개발하였음. 서버를 구입하여 외부에서 사용할 수 있도록 하는 정도까지는 구현하지 못하였으나, 가볍게 서버와 클라이언트를 나눠 클라이언트에서 민원을 문장 형태로 입력하면, 서버에서 토픽과 텍스트의 유사도를 활용하여 과거 민원을 추천해주는 형식으로 구현하였음.
