## 가려진 얼굴 복원 모델 

### 폴더 구조
```
DeepLearningSystem_main/
│
├── data/
│   ├── ffhq/
│   │   ├── 00000.zip
│   │   └── .....zip   -> zip파일 넣기
│   └── image/
│       ├── 00000
│       └── ....      -> zip파일 푼 파일      
│
├── all_half_masked/   
│   └── ......    -> 마스크 된 이미지 
├── all_half_mask_only/
│   └── ......    -> 마스크 부분 이미지
│  
├── buildmaskerData.py -> 실행시 all_half파일들 만들어짐
├── masker.py  -> 마스크 클래스
│ 
├── train_cbam.py    -> 훈련 파일
│
└── eval.py  -> 테스트 파일
```
