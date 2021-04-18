# Hybrid-Model-Enabling-Highly-Efficient-Follicular-Segmentation
## Introduction

### Abstract
The prevalence of thyroid cancer is growing rapidly.  Early and precise diagnosis is critical in thyroid cancer caring.  An automatic thyroid cancer diagnostic tool can be valuable to achieve early detection and diagnostic consistency.  Only the follicular areas in the sample contain useful information to the thyroid cancer diagnosis based on fine needle aspiration (FNA). This study aimed to develop a highly efficient accurate method for follicular cell areas segmentation (FCAS) of thyroid cytopathological whole slide images (WSIs).

A total of 96 cell samples from July 2017 to July 2018 in one hospital in Beijing, China were collected.  Forty-three WSIs were selected and manually labeled, including 17 cases of papillary thyroid carcinoma sample and 26 cases of benign sample.  6900 cropped typical image patches (available on our github) of 1024×1024 pixels from 13 large WSIs were used for patch-level model training and testing and all of the 13 large WSIs were papillary thyroid carcinoma samples.  Thirty testing WSIs with an average size 36,217×29,400 (from 10,240×10,240 to 81,920×61,440) were used to test the effectiveness of the hybrid model.  Based on the traditional semantic segmentation model deeplabv3, we constructed a hybrid segmentation architecture by adding a classification branch into the segmentation scheme to improve efficiency.  Accuracy was used to measure the performance of the classification model; pixel accuracy (pAcc), mean accuracy (mAcc), mean intersection over union (mIoU), and frequency weighted intersection over union (fwIoU) were used to measure the performance of the segmentation model, respectively.

### Problem
[comment]:<![](patch-examples/patch-examples.png)>
<img src="/patch-examples/figure1.png" width="800px"/>

1. Large size: the thyroid cytopathological WSIs, which are generated through an electronic scanner of the thin tumor sample, often are in a very large size (for example, 19,6608×94,208). The typical size of a single slide is tens of gigabytes, thus it exceeds GPUs memory limitations.

2. The effective data area is small and sparsely distributed： each thyroid WSI slide often contains follicular areas, colloid areas, and the other blank background areas. Only the follicular areas as denoted by the blue points in the above figure, which often occupy less than 2% area in a thyroid WSI, contain useful information to the thyroid cancer diagnosing.


### Architecture Overview
<img src="/patch-examples/figure2.png" width="800px"/>

### Highlights
1. Fast segmentation of follicular areas
2. Hybrid architecture by integrating classification branch and segmeatation branch

## Citation
Please cite this paper in your publications if it helps your research:
```
Extended journal version: coming soon!
```


Workshop version: [AAAI_Workshop](https://arxiv.org/pdf/1902.05431.pdf)
```
@inproceedings{tao2019highly,
  title={Highly efficient follicular segmentation in thyroid cytopathological whole slide image},
  author={Tao, Siyan and Guo, Yao and Zhu, Chuang and Chen, Huang and Zhang, Yue and Yang, Jie and Liu, Jun},
  booktitle={International Workshop on Health Intelligence},
  pages={149--157},
  year={2019},
  organization={Springer}
}
```
## Dataset
<img src="/patch-examples/patch-examples.png" width="500px"/>

You can download the patch dataset (about 10G) through 链接: https://pan.baidu.com/s/1JcOXFklZKLOcHEexvtFLjQ  

To obtain the password pls email me: czhu@bupt.edu.cn 


## Authors
Siyan Tao, Minzhen Li, Chuang Zhu:
- email: tao_siyan@163.com；1421887087@qq.com；czhu@bupt.edu.cn
- wechat: lmz__120189

If you have any questions, you can contact me directly.
