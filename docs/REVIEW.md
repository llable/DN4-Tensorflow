# Paper Review of DN4

## Paper Information
<li>Paper Name: Revisiting Local Descriptor based Image-to-Class Measure for Few-shot Learning.</li>
<li>Authors: Wenbin Li, Lei Wang, Jinglin Xu, Jing Huo, Yang Gao and Jiebo Luo.</li>
<li>Acceptance: In CVPR 2019.</li>

## Fundamental studies
 - Few-shot learning
    > Meta-learning based, Metric-learning based, Image-level feature based measure
 - Image classification
 - Naive-Bayes Nearest Neighbor(NBNN)

## Contribution
- 기존의 image-level feature기반의 Few-shot learning 기법이 가지는 적은 examples에서의 한계를 보완
- 성능 뿐만아니라 위의 실험환경과 같이 efficiency 또한 높힘
   > 실험환경: Nvidia GTX 1080Ti GPU, Intel i7-3820 CPU 각 하나씩

## Methods
 - 기존의 Few-shot learning에서는 이미지 분류에 있어서 image-level feature 기반 측정이 대체로 사용
 - 저자는 이 같은 방법을 Naive-bayes Nearest Neighbor(NBNN)에서 영감을 받아 두 가지 문제점을 발견함
    > - Local features를 image-level 표현법으로 압축하면 정보 손실이 일어나고 training 예제가 적을 경우 이는 복구되지 않음
    > - 이 때 얻은 정보인 local features들을 image-to-image 측정에 사용하는 것을 적합하지 않음.
 - 이를 토대로 저자는 image-to-image 기법을 iamge-to-class 기법을 기반으로한 local descriptor로서 네트워크를 설계함으로서 기존의 Few-shot learning 기법들이 가지는 한계를 보완하려함.
    > 명칭은 Deep Nearest Neighbor Neural Network의 준말인 DN4. 

## Proposed Architecture
<img src="/docs/images/Architecture.PNG" width="700px">
 - Deep local descriptor들의 학습을 위한 CNN 기반의 임베딩 모듈, 주어진 이미지와 각 클래스간의 유사도를 측정하기 위한 image-to-class module로 구성
 - deep local descriptor 모듈: 모든 이미지에 대해서 학습
 - image-to-class 모듈: 각 클래스에 대해서 k-NN을 이용하여 유사도를 측정
 
 ## Datasets
  - 본 논문에서는 4가지의 데이터셋을 벤치마킹하여 실험에 사용함
  - miniImageNet
  - Stanford Dogs
  - Stanford Cars
  - CUB-200

## Discussion of Expermients 
TBD with [reproducing the paper](https://github.com/llable/DN4-Tensorflow) :) 
