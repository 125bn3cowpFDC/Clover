# Find Clover
- Language : Python
- Framework&Model : Yolov3
- 특이사항 : 실행 환경별 모델 혹은 실행환경 업데이트 요망
---
## Dataset
resizing


![clover_resize](https://github.com/125bn3cowpFDC/Clover/assets/170291905/cd2b9c36-6dce-4fd0-a294-7328d69eeca9)

- 모델 input사이즈 416x416규격 적용

normal dataset


![normal](https://github.com/125bn3cowpFDC/Clover/assets/170291905/a59ea8f0-379d-4e13-80cd-90141517d820)


- row-data에서 resizing만 진행된 상태의 이미지의 영역

edge dataset


![edge](https://github.com/125bn3cowpFDC/Clover/assets/170291905/b48c2626-2bf7-4e43-9bb3-37b7e9029542)
- canny-edge를 적용한 상태의 이미지 영역

small area dataset


![small](https://github.com/125bn3cowpFDC/Clover/assets/170291905/d0d2474e-3e04-4d87-89f5-7d1944d4983d)

- 클로버의 잎 중심 기준 normal dataset보다 작은 영역

augmentation dataset


![aug](https://github.com/125bn3cowpFDC/Clover/assets/170291905/66a4f002-cdc9-47e1-858d-4e968b2d79f8)
- horizontal, vertical flip을 통해 데이터 augmentation된 이미지의 영역
---
## Result
normal dataset


![n_](https://github.com/125bn3cowpFDC/Clover/assets/170291905/7e5b56bd-b3ff-45d4-ac8d-fc5abbd6229b)


**결과**

- **mAP 70%**
- **IoU 38% (실제 이미지 예측에 대하여 네잎클로버는 잘 찾았지만 IoU가 38%정도로 낮음.)**


small area dataset


![s_](https://github.com/125bn3cowpFDC/Clover/assets/170291905/1e0e5c4e-6209-4e60-ac72-03c7dc59cbfc)


**결과**

- **mAP 70% - normal dataset과 유사.**
- **IoU 78% - 잘못된 객체 포함 검출.**

edge dataset


![e_](https://github.com/125bn3cowpFDC/Clover/assets/170291905/26304f98-2e31-4a7b-a3a3-f95caf75f5a2)
**결과**

- **mAP 54% - 선행된 dataset보다 낮음.**
- **IoU 26% - 선행된 dataset보다 낮음.**

augmentation dataset


![aug_](https://github.com/125bn3cowpFDC/Clover/assets/170291905/e995483d-d6d0-4368-b0d7-b1928f6b6121)
**결과**

- **mAP 86%**
- **IoU 39% - normal dataset보다 미약하게 개선됨**
