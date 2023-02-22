# Bagging R-CNN

This is the official code for 「Bagging R-CNN: Ensemble for object detection in complex traffic scenes」.

🚩 Our paper is accepted by ICASSP 2023.

![framework](https://user-images.githubusercontent.com/48271804/220507165-c3276b4a-1449-4cb7-8b9e-6cf2b6dba00a.png)

Generic object detection methods have achieved preferable results, but it is still challenging to detect objects from complicated traffic scenes like extreme illumination and adverse weather. The existing methods are not robust enough to be extended to new complex traffic scenes. To address this issue, we leverage the idea of ensemble learning for strong robustness and propose a novel Bagging R-CNN framework. Specially, we design a bagging classification branch that uses adaptive sampling to train base learners and make them different from each other. The final predictions are the ensemble of the base learners, achieving strong robustness to the challenging objects. For localizing more accurately, a progressive regression branch is proposed in which bounding boxes are continuously optimized for high quality. Extensive experiment results on TJU-DHD-traffic and Pascal VOC datasets show that our Bagging R-CNN achieves superior detection accuracy over state-of-the-art methods.


