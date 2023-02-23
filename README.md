# Bagging R-CNN

This is the official code for 「Bagging R-CNN: Ensemble for object detection in complex traffic scenes」.

Wait to complete the code .......

🚩 Our paper is accepted by ICASSP 2023.

![framework](https://user-images.githubusercontent.com/48271804/220507165-c3276b4a-1449-4cb7-8b9e-6cf2b6dba00a.png)

## Abstract

Generic object detection methods have achieved preferable results, but it is still challenging to detect objects from complicated traffic scenes like extreme illumination and adverse weather. The existing methods are not robust enough to be extended to new complex traffic scenes. To address this issue, we leverage the idea of ensemble learning for strong robustness and propose a novel Bagging R-CNN framework. Specially, we design a bagging classification branch that uses adaptive sampling to train base learners and make them different from each other. The final predictions are the ensemble of the base learners, achieving strong robustness to the challenging objects. For localizing more accurately, a progressive regression branch is proposed in which bounding boxes are continuously optimized for high quality. Extensive experiment results on TJU-DHD-traffic and Pascal VOC datasets show that our Bagging R-CNN achieves superior detection accuracy over state-of-the-art methods.

## Preparation

### Installation

Follow the mmdetection. https://github.com/open-mmlab/mmdetection

### Data preparation

https://github.com/tjubiit/TJU-DHD

We need to download the TJU-DHD-traffic 「training & validation set」and its annotations.

We also prepare the corresponding data config file of TJU-DHD-traffic,and you can find it in the 

## Get start

1. Use single GPU
```
CUDA_VISIBLE_DEVICES=0,1,2,3 PORT=29500 ./tools/dist_train.sh ${CONFIG_FILE} 4
```

2. Use several GPUs
```
CUDA_VISIBLE_DEVICES=0 PORT=29500 ./tools/dist_train.sh ${CONFIG_FILE} 1
```

## Our method 

Our method is simple and effiient, which is motivated by Cascade RCNN and Ensemble learning. If you want to understand our method directly and have used the mmdetection, you can read the file.

## Acknowledgements

🐭 Thanks to Pinhao Song「AKA.Shenzhen Pilot」. His master's research field is underwater object detection. 
[Google Research](https://scholar.google.com.hk/citations?user=pgD4ZGgAAAAJ&hl=zh-CN&oi=sra) | [Github](https://github.com/mousecpn)

🏳️ This work is also the advance work of [Boosting R-CNN](https://www.sciencedirect.com/science/article/pii/S0925231223001200), which is accepted by Neurocomputing 2023.
