# Attention-Guided Pyramid Context Network for Polyp Segmentation in Colonoscopy Images
Guanghui Yue, Siying Li, Runmin Cong, Tianwei Zhou, Baiying Lei, and Tianfu Wang

## 1. Overview

### 1.1. Introduction

Recently, deep convolutional neural networks (CNNs) have provided us an effective tool for automated polyp segmentation in colonoscopy images. However, most CNN-based
methods do not fully consider the feature interaction among different layers and often cannot provide satisfactory segmentation performance. In this paper, a novel attention-guided pyramid context network (APCNet) is proposed for accurate and robust polyp segmentation in colonoscopy images. Specifically, considering that different network layers represent the polyp in different aspects, APCNet first extracts multi-layer features in a pyramid structure, then utilizes an attention-guided multi-layer aggregation strategy to refine the context features of each layer by utilizing the complementary information of different layers. To obtain abundant context features, APCNet employs a context extraction module that explores the context information of each layer via local information retainment and global information compaction. Through the top-down deep supervision, our APCNet implements a coarse-to-fine polyp segmentation and finally localizes the polyp region precisely. Extensive experiments on two in-domain and four out-of-domain experiments show that APCNet is comparable to 19 state-of-the-art methods. Moreover, it holds a more appropriate trade-off between effectiveness and computational complexity than these competing methods.
 
### 1.2. Clone repository

```shell
git clone https://github.com/lisiying-eazin/APCNet.git
cd APCNet/
```

## 2. Proposed Baseline

### 2.1. Training/Testing:

Downloading necessary data:
The training and testing datasets come from [PraNet](https://github.com/DengPingFan/PraNet). Download these datasets and unzip them into "data" folder

+ downloading testing dataset and move it into `./data/TestDataset/`, 
    which can be found in this [download link (Google Drive)](https://drive.google.com/file/d/1o8OfBvYE6K-EpDyvzsmMPndnUMwb540R/view?usp=sharing). It contains five sub-datsets: CVC-300 (60 test samples), CVC-ClinicDB (62 test samples), CVC-ColonDB (380 test samples), ETIS-LaribPolypDB (196 test samples), Kvasir (100 test samples).
    
+ downloading training dataset and move it into `./data/TrainDataset/`, 
    which can be found in this [download link (Google Drive)](https://drive.google.com/file/d/1lODorfB33jbd-im-qrtUgWnZXxB94F55/view?usp=sharing). It contains two sub-datasets: Kvasir-SEG (900 train samples) and CVC-ClinicDB (550 train samples).
    
### 2.2. Download model:

+ If you want to test the performance of APCNet, please download our trained model 
    which can be found in this [download link (Google Drive)](https://drive.google.com/file/d/1eUIGcCFTPoUhWNALyG5nqJR_yJDyPAXA/view?usp=share_link)

### 2.3 Evaluating your trained model:

Matlab: One-key evaluation is written in MATLAB code ([link](https://drive.google.com/file/d/1_h4_CjD5GKEf7B1MRuzye97H0MXf2GE9/view?usp=sharing)), 
please follow this the instructions in `./eval/main.m` and just run it to generate the evaluation results in `./res/`.
The complete evaluation toolbox (including data, map, eval code, and res): [new link](https://drive.google.com/file/d/1bnlz7nfJ9hhYsMLFSBr9smcI7k7p0pVy/view?usp=sharing). 

Python: Please refer to the work of ACMMM2021 https://github.com/plemeri/UACANet

### 2.4. Prediction maps:

+ predcitions maps of testing dataset of models, 
    which can be found in this [download link (Google Drive)](https://drive.google.com/file/d/1f8OUcthoo8YWcKR-txqJsgNqudLeYXe1/view?usp=share_link)
