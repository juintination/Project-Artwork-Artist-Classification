# Project-Artwork-Artist-Classification
Implementation of an AI model that allows 50 artists to be classified into accurate artist classification for a test dataset given only a fraction of the artwork

---

## 월간 데이콘 예술 작품 화가 분류 AI 경진대회

- 대회 안내
  - 예술 작품의 일부만 주어진 테스트 데이터 세트에 대해 50명의 예술가를 정확한 예술가 분류로 분류할 수 있는 AI 모델 구현
- Dataset Info.
  - train [폴더] : 학습용 예술 작품 이미지(0000.jpg ~ 5910.jpg (5911개))
  - test [폴더] : 예술 작품의 일부분(약 1/4)의 이미지(TEST_00000.jpg ~ TEST_12669.jpg (12670개))
  - train.csv [파일] : 5911개(0000.jpg ~ 5910.jpg)의 이미지의 경로가 적힌 csv 파일, 그 중 5320개의 이미지로 학습하였고 591개의 이미지를 validation 데이터로 split 하여 성능을 확인하였음
  - test.csv [파일] : 12670개(TEST_00000.jpg ~ TEST_12669.jpg)의 예술 작품의 일부분(약 1/4)의 이미지의 경로가 적힌 csv 파일
  - artists_info.csv [파일] : 학습에 추가로 활용할 수 있는 화가 정보(name : 화가 이름, years, genre, nationality)
  - sample_submission.csv [파일] : 제출양식(id : 샘플 별 고유 id, artist : 분류한 화가 이름)
- 주최 / 주관 : 데이콘

---

## 파일 설명
1. Resnet50image_crop_load.ipynb : Resnet50 모델 사용, 이미지의 가운데 부분을 정사각형으로 잘라 244X244 크기로 resize하는 방식으로 전처리
2. Resnet50image_load.ipynb : Resnet50 모델 사용, 이미지를 바로 244X244 크기로 resize하는 방식으로 전처리
3. Resnet50withImageGenerator (1).ipynb : Resnet50 모델 사용, ImageGenerator을 사용하여 전처리, callbacks=([early_stopping])
4. Resnet50withImageGenerator (2).ipynb : Resnet50 모델 사용, ImageGenerator을 사용하여 전처리, epochs=10
5. Resnet50withImageGenerator (3).ipynb : Resnet50 모델 사용, ImageGenerator을 사용하여 전처리, epochs=20
6. VGG19withImageGenerator (1).ipynb : VGG19 모델 사용, ImageGenerator을 사용하여 전처리, epochs=10
7. VGG19withImageGenerator (2).ipynb : VGG19 모델 사용, ImageGenerator을 사용하여 전처리, epochs=20
8. VGG19withImageGenerator (3).ipynb : VGG19 모델 사용, ImageGenerator을 사용하여 전처리, epochs=50
9. VGG19withImageGenerator (4).ipynb : VGG19 모델 사용, ImageGenerator을 사용하여 전처리, epochs=100
10. GooglenetWithImageGenerator (1).ipynb : InceptionV3 모델 사용, ImageGenerator을 사용하여 전처리, epochs=20
11. GooglenetWithImageGenerator (2).ipynb : InceptionV3 모델 사용, ImageGenerator을 사용하여 전처리, epochs=50
12. Resnet50withClassWeight (1).ipynb : Resnet50 모델 사용, ImageGenerator을 사용하여 전처리 및 ClassWeight 적용, epochs=20, dropout=0.2
13. Resnet50withClassWeight (2).ipynb : Resnet50 모델 사용, ImageGenerator을 사용하여 전처리 및 ClassWeight 적용, epochs=20, dropout=0.5
14. GooglenetWithClassWeight (1).ipynb : InceptionV3 모델 사용, ImageGenerator을 사용하여 전처리 및 ClassWeight 적용, epochs=10
15. GooglenetWithClassWeight (2).ipynb : InceptionV3 모델 사용, ImageGenerator을 사용하여 전처리 및 ClassWeight 적용, epochs=50

---

## 기타 사항

- 지도교수 : 정은성 교수님

- 개발환경 : <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=Python&logoColor=white"> <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=Jupyter&logoColor=white">

## 참고

- [월간 데이콘 예술 작품 화가 분류 AI 경진대회 링크](https://dacon.io/competitions/official/236006/overview/description)
- [데이터 노이즈 관련 (id 3896, 3986) 링크](https://dacon.io/competitions/official/236006/talkboard/407044?page=1&dtype=recent)
