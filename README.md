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
### 사용방법
> #### 환경설정
> 기본 환경 cuda 11.8 / 리눅스 20.04 / .GPU : RTX 3060
> 1. ```conda create -n myenv python=3.9 -y```
> 2. ```conda activate myenv```
> 3. ```pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118```
> 4. ```pip install pandas opencv-python numpy tqdm matplotlib```
> 5. ```pip install scikit-learn pillow scikit-image lpips pytorch-fid```

> #### 코드 실행 
> 1. ```python buildmaskerData.py``` 실행해서 데이터 파일 만들기.
> 2. ```python train_cbam.py``` 훈련 시작
> 3. ```python eval.py```  평가하기
