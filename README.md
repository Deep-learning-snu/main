# Python
 딥러닝의 통계적이해 수업 프로젝트 팀입니다. 2022-09-27 ~

## 스터디 방식
- ⏰ 스터디 시간 : 매주 수 오후 3시
- 📗 스터디 자료 : [딥러닝 수업 오티](https://won-j.github.io/M1399_000400-2022fall/), [산림청 국립수목원_버섯자원서비스](https://www.data.go.kr/tcs/dss/selectApiDataDetailView.do?publicDataPk=15056525)
  - 딥러닝을 분석하여 노트(Jupyter notebook)에 정리
  - 제안, 질문은 [Issues](https://github.com/deep-dive-in-python/main/issues) 를 이용
  
## 스터디 자료
- [캐글 스터디 커리큘럼](https://kaggle-kr.tistory.com/32)
- [Alexnet](https://www.cognex.com/ko-kr/blogs/deep-learning/research/deep-learning-image-classification-dogs-vs-cats-classification-alexnet)
- [다른 방법론](https://medium.com/ddiddu-log/%EC%9D%B4%EB%AF%B8%EC%A7%80-%EC%9D%B8%EC%8B%9D%EC%9D%98-%EC%A0%95%EC%9D%98%EC%99%80-%EC%A3%BC%EC%9A%94-%EB%AA%A8%EB%8D%B8-%EB%B9%84%EA%B5%90-1-%EC%9D%B4%EB%AF%B8%EC%A7%80-%EB%B6%84%EB%A5%98-image-classification-ae7a59bfaf65)
- [CNN 데이터 전처리](https://rdmkyg.blogspot.com/2021/06/cnn-cat-and-dog-dataset.html) 
- [generative model](https://intrepidgeeks.com/tutorial/aiffel-22028-creates-unprecedented-new-fashion-with-artificial-intelligence)
- [CNN basic 1](https://yjjo.tistory.com/8)
- [CNN basic 2](https://datasirup.tistory.com/m/117)
- [Data augmentation](https://www.geeksforgeeks.org/python-data-augmentation/)
- [딥러닝 이미지 분류 논문 10개 선별](https://bigsong.tistory.com/47)
- [MOAT 논문](https://arxiv.org/pdf/2210.01820.pdf) - [코드](https://github.com/google-research/deeplab2)
- [MOAT github](https://github.com/RooKichenn/pytorch-MOAT)
- [Efficient Adaptive Ensembling 논문](https://arxiv.org/pdf/2206.07394.pdf)
- [맥북 M1 Tensorflow 설치](https://velog.io/@pcj1541/1.-Macbook-M1-Tensorflow-설치하기for-jupyter-notebook)
- [Tensorflow 기본 사용법](https://tensorflowkorea.gitbooks.io/tensorflow-kr/content/g3doc/get_started/basic_usage.html)
- [Tensorflow CNN 강의](https://opentutorials.org/module/5268/29787)
----
 - Dataset
   - [car196](https://www.tensorflow.org/datasets/catalog/cars196)
### 간편 Git 사용 방법
  - Git clone
```
git clone https://github.com/Deep-learning-snu/main.git
```
  - Git 다운받기
```
git pull
```
  - Git 올리기
```
git add .
git commit -am "message"
git push 
```

## 논문 레퍼런스 추가하는 방법
1. 논문 사이트에 들어가 download citation-BibTex 복사하기.
2. overleaf에 reference.bib 파일에 복사 붙여넣기.
3. main.tex에 쓸 때는 논문 관련 단어\cite{논문 이름} 으로 추가하기.

## 프로젝트 기록
### Binary classification-독버섯 분류기
- 2022-09-28-수 3시
  - 프로젝트 계획 수립-독버섯 분류기
  - 버섯 도감을 보고 독버섯인지 아닌지 label하고 이미지 크롤링으로 버섯의 이미지 가져오기.
  - CNN, Binary classification-어떤 방법론 이용할지
  - 버섯도감 파이썬으로 크롤링(경선), 이미지 크롤링(다연, 동욱)

- 2022-10-05-수 3시
  - 제안서 양식이나 발표 형식, 분 알아오기
  - 1.이미지 픽셀 차원 동일화 + 독버섯이다 아니다 라벨링 + 이미지 픽셀 matrix로 변환(다연)
  - 2.기본적인 CNN 올리고 돌리기(경선)
  - 3.CNN 내부 요소 바꿔서 스코어 확인(동욱)
  - 버섯 데이터에 문제가 조금 있으므로 만약에 바꾼다면 어떤 데이터로 할지 생각해오기
------
### 다른 주제 선정 회의 결과: 건물분류 지도학습, (패턴생성 vae,건물분류 비지도학습 탈락)
- 역할분담
  - 이미지 크롤링/라벨링 - 동욱
  - 이미지 정제(관련 없는 이미지 제거/픽셀 통일) - 다연
  - 이미지 임베딩 - 경선
  
- [음식 이미지 분류](https://www.tensorflow.org/datasets/catalog/food101)
 > [대형폐기물 분류](https://data.seoul.go.kr/etc/aiEduData.do)
- data augmentation 
- vanilla cnn, cnn, ResNet, VGG-16 돌리고 비교, 앙상블, 개조, 최신 방법론 이용할 수 있으면 좋고

--------
### 딥러닝 프로포절 발표 피드백
- 단순히 기존의 방법들을 앙상블하여 accuracy를 높이는 것은 수업의 방향과 맞지 않음.
- 따라서 방법론의 한계를 찾고 이를 개선하는 식의 노력이 필요.
--------
- 2022-10-24-월 3시
  - 동욱: MaxViT-L MaxViT: Multi-Axis Vision Transformer
    - PolyLoss: A Polynomial Expansion Perspective of Classification Loss Functions 으로 수정 
  - 다연: MOAT-4 22K+1K MOAT: Alternating Mobile Convolution and Attention Brings Strong Vision Models
  - 경선: TWIST (ResNet-50) Self-Supervised Learning by Estimating Twin Class Distributions
  - [image classification rank](https://paperswithcode.com/sota/image-classification-on-imagenet)
  - [food 101 classification](https://paperswithcode.com/sota/image-classification-on-food-101-1)
  - 각자 페이퍼 읽고 한계점 알아오고 그것의 개선 아이디어 하나씩. 
------
- 2022-10-29-토 10시
  - 경선: TWIST 모델링에 fairness term을 추가해서 biased dataset의 성능을 높이자!
  - 동욱: polyloss , adaptive ensemble
  - 다연: moat scaling rule 바꿔보자!
  - MOAT 다들 공부해서 
------
- 2022-11-10-고통방 끝나고 모이기
  - 1. 진행상황 피드백 하기. Tiny moat 구현, 공부해오기 , pre train model 불러오기. 11/16
  - 2. Food dataset에 맞춰서 Input output 바꾸기 
  - 3. 각 모델의 train된 weight 고정하고 마지막 레이어 합쳐서 마지막 레이어만 train 시키기. tensorflow에서 stacking 구현 11/30
-----
 - 2022-11-21-3시
  - 마지막 아웃픗 101짜리 벡터로 바꾸기 softmax, 5개짜리 z로 input, data augmentation 완성, moat와 붙여서 

------
 - 2022-11-29-화
   - paper와 presentation 쓸 사람 나누기
   - 경선: Abstract & Introduction & Summary & Reference
   - 다연: Experiment
   - 동욱: Main Framework
