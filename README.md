# Awesome Knowledge Distillation for Object Detection [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

[![lint](https://github.com/LutingWang/awesome-knowledge-distillation-for-object-detection/actions/workflows/lint.yaml/badge.svg)](https://github.com/LutingWang/awesome-knowledge-distillation-for-object-detection/actions/workflows/lint.yaml)

A curated list of **awesome** distillation techniques designed for object detectors.

Parameters compression and accuracy boosting are core problems for object detection towards practical application, where knowledge distillation (KD) is one of the most popular solutions.
KD aims at training the compact model (student) by transferring knowledge from a high-capacity model (teacher).
Papers and codes are listed.

## Contents

- [Knowledge Distillation for General Object Detectors](#knowledge-distillation-for-general-object-detectors)
  - [Feature Distillation](#feature-distillation)
    - [Foreground Masks](#foreground-masks)
      - [Ground Truth Guided](#ground-truth-guided)
      - [Prediction Guided](#prediction-guided)
      - [Attention Guided](#attention-guided)
      - [Miscellaneous Foreground Masks](#miscellaneous-foreground-masks)
    - [Miscellaneous Feature Distillation](#miscellaneous-feature-distillation)
  - [Instance Distillation](#instance-distillation)
  - [Label Assignment Distillation](#label-assignment-distillation)
  - [Balancing between Tasks](#balancing-between-tasks)
  - [Miscellaneous Knowledge Distillation for General Object Detectors](#miscellaneous-knowledge-distillation-for-general-object-detectors)
- [Knowledge Distillation for Specific Object Detectors](#knowledge-distillation-for-specific-object-detectors)
  - [Knowledge Distillation for GFL](#knowledge-distillation-for-gfl)
  - [Knowledge Distillation for DETR](#knowledge-distillation-for-detr)
- [Knowledge Distillation for Heterogeneous Object Detectors](#knowledge-distillation-for-heterogeneous-object-detector-pairs)
- [Teacher Free Knowledge Distillation for Object Detectors](#teacher-free-knowledge-distillation-for-object-detectors)
- [Miscellaneous](#miscellaneous)
- [Newly Published Papers](#newly-published-papers)

## Knowledge Distillation for General Object Detectors

*NeurIPS 2017*.
\[[NeurIPS](https://proceedings.neurips.cc/paper/2017/hash/e1e32e235eee1f970470a3a6658dfdd5-Abstract.html)\]
\- A new framework to learn compact and fast object detection networks with improved accuracy using knowledge distillation and hint learning.

- Learning Efficient Object Detection Models with Knowledge Distillation
- Guobin Chen and Wongun Choi and Xiang Yu and Tony Han and Manmohan Chandraker

Mimic. *CVPR 2017*.
\[[CVF](http://openaccess.thecvf.com/content_cvpr_2017/html/Li_Mimicking_Very_Efficient_CVPR_2017_paper.html)\]
\[[IEEE Xplore](http://ieeexplore.ieee.org/abstract/document/8100259/)\]
\- A fully convolutional feature mimic framework to train very efficient CNN based detectors, which do not need ImageNet pre-training and achieve competitive performance as the large and slow models.

- Mimicking Very Efficient Network for Object Detection
- Quanquan Li and Shengying Jin and Junjie Yan

### Feature Distillation

#### Foreground Masks

##### Ground Truth Guided

FGFI. *CVPR 2019*.
\[[CVF](http://openaccess.thecvf.com/content_CVPR_2019/html/Wang_Distilling_Object_Detectors_With_Fine-Grained_Feature_Imitation_CVPR_2019_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/8953432/)\]
\[[arXiv](http://arxiv.org/abs/1906.03609)\]
<[GitHub](https://github.com/twangnh/Distilling-Object-Detectors)>
\- A fine-grained feature imitation method exploiting the cross-location discrepancy of feature response.

- Distilling Object Detectors With Fine-Grained Feature Imitation
- Tao Wang and Li Yuan and Xiaopeng Zhang and Jiashi Feng

DeFeat. *CVPR 2021*.
\[[CVF](http://openaccess.thecvf.com/content/CVPR2021/html/Guo_Distilling_Object_Detectors_via_Decoupled_Features_CVPR_2021_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9578919/)\]
\[[arXiv](http://arxiv.org/abs/2103.14475)\]
\- A novel distillation algorithm via decoupled features for learning a better student detector.

- Distilling Object Detectors via Decoupled Features
- Jianyuan Guo and Kai Han and Yunhe Wang and Han Wu and Xinghao Chen and Chunjing Xu and Chang Xu

##### Prediction Guided

FRS. *NeurIPS 2021*.
\[[NeurIPS](https://proceedings.neurips.cc/paper_files/paper/2021/hash/29c0c0ee223856f336d7ea8052057753-Abstract.html)\]
\[[OpenReview](https://openreview.net/forum?id=_bOfK2k_7R)\]
\[[arXiv](http://arxiv.org/abs/2111.00674)\]
\- A novel Feature-Richness Score (FRS) method to choose important features that improve generalized detectability during distilling.

- Distilling Object Detectors with Feature Richness
- Zhixing Du and Rui Zhang and Ming Chang and Xishan Zhang and Shaoli Liu and Tianshi Chen and Yunji Chen

PGD. *ECCV 2022*.
\[[ECVA](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136690123.pdf)\]
\[[Springer](https://link.springer.com/chapter/10.1007/978-3-031-20077-9_8)\]
\[[arXiv](http://arxiv.org/abs/2203.05469)\]
<[GitHub](https://github.com/ChenhongyiYang/PGD)>
\- Distill on the key predictive regions of the teacher.

- Prediction-Guided Distillation for Dense Object Detection
- Chenhongyi Yang and Mateusz Ochal and Amos Storkey and Elliot J Crowley

TBD. *PR*.
\[[ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0031320323000213)\]
\[[arXiv](https://arxiv.org/abs/2208.03006)\]
\- Alleviates the misalignment between classification score and localization quality via Harmony Score and Task-Balanced Distillation.

- Task-balanced distillation for object detection
- Ruining Tang and Zhenyu Liu and Yangguang Li and Yiguo Song and Hui Liu and Qide Wang and Jing Shao and Guifang Duan and Jianrong Tan

##### Attention Guided

FKD. *ICLR 2021*.
\[[OpenReview](https://openreview.net/forum?id=uKhGRvM8QNH)\]
<[GitHub](https://github.com/ArchipLab-LinfengZhang/Object-Detection-Knowledge-Distillation-ICLR2021)>
\- Attention-guided distillation and non-local distillation.

- Improve Object Detection with Feature-based Knowledge Distillation: Towards Accurate and Efficient Detectors
- Chunting Zhou and Graham Neubig and Jiatao Gu

FKD. *TPAMI*.
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/10198386/)\]
\- A structured knowledge distillation scheme, including attention-guided distillation and non-local distillation.

- Structured Knowledge Distillation for Accurate and Efficient Object Detection
- Linfeng Zhang and Kaisheng Ma

FGD. *CVPR 2022*.
\[[CVF](https://openaccess.thecvf.com/content/CVPR2022/html/Yang_Focal_and_Global_Knowledge_Distillation_for_Detectors_CVPR_2022_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9879869/)\]
\[[arXiv](http://arxiv.org/abs/2111.11837)\]
<[GitHub](https://github.com/yzd-v/FGD)>
\- Focal distillation separates the fore-ground and background, while global distillation rebuilds the relation between different pixels and transfers it from teachers to students.

- Focal and Global Knowledge Distillation for Detectors
- Zhendong Yang and Zhe Li and Xiaohu Jiang and Yuan Gong and Zehuan Yuan and Danpei Zhao and Chun Yuan

GLAMD. *ECCV 2022*.
\[[ECVA](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136700456.pdf)\]
\[[Springer](https://link.springer.com/chapter/10.1007/978-3-031-20080-9_27)\]
\- Divide the feature maps into several patches and apply an attention mechanism for both the entire feature area and each patch.

- GLAMD: Global and Local Attention Mask Distillation for Object Detectors
- Younho Jang and Wheemyung Shin and Jinbeom Kim and Simon Woo and Sung-Ho Bae

##### Miscellaneous Foreground Masks

CD. *ICCV 2021*.
\[[CVF](http://openaccess.thecvf.com/content/ICCV2021/html/Shu_Channel-Wise_Knowledge_Distillation_for_Dense_Prediction_ICCV_2021_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9710762/)\]
\[[arXiv](http://arxiv.org/abs/2011.13256)\]
<[GitHub](https://github.com/irfanICMLL/TorchDistiller/tree/main/SemSeg-distill)>
\- Normalize the activation map of each channel to obtain a soft probability map.

- Channel-wise Knowledge Distillation for Dense Prediction
- Changyong Shu and Yifan Liu and Jianfei Gao and Zheng Yan and Chunhua Shen

#### Miscellaneous Feature Distillation

DRKD. *IJCAI 2023*.
\[[arXiv](https://arxiv.org/abs/2302.05637)\]
\- Dual relation knowledge distillation, including pixel-wise relation distillation and instance-wise relation distillation

- Dual Relation Knowledge Distillation for Object Detection
- Zhenliang Ni and Fukui Yang and Shengzhao Wen and Gang Zhang

### Instance Distillation

GID. *CVPR 2021*.
\[[CVF](http://openaccess.thecvf.com/content/CVPR2021/html/Dai_General_Instance_Distillation_for_Object_Detection_CVPR_2021_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9577671/)\]
\[[arXiv](http://arxiv.org/abs/2103.02340)\]
\- A novel distillation method for detection tasks based on discriminative instances without considering the positive or negative distinguished by GT.

- General Instance Distillation for Object Detection
- Xing Dai and Zeren Jiang and Zhao Wu and Yiping Bao and Zhicheng Wang and Si Liu and Erjin Zhou

DSIG. *ICCV 2021*.
\[[CVF](http://openaccess.thecvf.com/content/ICCV2021/html/Chen_Deep_Structured_Instance_Graph_for_Distilling_Object_Detectors_ICCV_2021_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9711100/)\]
\[[arXiv](http://arxiv.org/abs/2109.12862)\]
<[GitHub](https://github.com/dvlab-research/Dsig)>
\- A simple knowledge structure to exploit and encode information inside the detection system to  facilitate detector knowledge distillation.

- Deep Structured Instance Graph for Distilling Object Detectors
- Yixin Chen and Pengguang Chen and Shu Liu and Liwei Wang and Jiaya Jia

ICD. *NeurIPS 2021*.
\[[NeurIPS](https://proceedings.neurips.cc/paper_files/paper/2021/hash/892c91e0a653ba19df81a90f89d99bcd-Abstract.html)\]
\[[OpenReview](https://openreview.net/forum?id=k7aeAz4Vbb)\]
\[[arXiv](http://arxiv.org/abs/2110.12724)\]
<[GitHub](https://github.com/MegEngine/ICD)>
\- An instance-conditional distillation framework to find desired knowledge.

- Instance-Conditional Knowledge Distillation for Object Detection
- Zijian Kang and Peizhen Zhang and Xiangyu Zhang and Jian Sun and Nanning Zheng

### Label Assignment Distillation

LAD. *WACV 2022*.
\[[CVF](https://openaccess.thecvf.com/content/WACV2022/html/Nguyen_Improving_Object_Detection_by_Label_Assignment_Distillation_WACV_2022_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9706993/)\]
\[[arXiv](http://arxiv.org/abs/2108.10520)\]
<[MMDet](https://github.com/open-mmlab/mmdetection/tree/master/configs/lad)>
\- Use the teacher network to generate labels for the student, through the hard labels dynamically  assigned by the teacher.

- Improving Object Detection by Label Assignment Distillation
- Chuong H. Nguyen and Thuy C. Nguyen and Tuan N. Tang and Nam L. H. Phan

### Balancing between Tasks

TADF.
\[[arXiv](http://arxiv.org/abs/2006.13108)\]
\- A general distillation framework that adaptively transfers knowledge from teacher to student  according to the task specific prior.

- Distilling Object Detectors with Task Adaptive Regularization
- Ruoyu Sun and Fuhui Tang and Xiaopeng Zhang and Hongkai Xiong and Qi Tian

BCKD. *ICCV 2023*
\[[CVF](https://openaccess.thecvf.com/content/ICCV2023/html/Yang_Bridging_Cross-task_Protocol_Inconsistency_for_Distillation_in_Dense_Object_Detection_ICCV_2023_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/10377607)\]
\[[arXiv](http://arxiv.org/abs/2308.14286)\]
\- A novel distillation method with cross-task consistent protocols, tailored for the dense object detection.

- Bridging Cross-task Protocol Inconsistency for Distillation in Dense Object Detection
- Longrong Yang and Xianpan Zhou and Xuewei Li and Liang Qiao and Zheyang Li and Ziwei Yang and Gaoang Wang and Xi Li

### Miscellaneous Knowledge Distillation for General Object Detectors

*AAAI 2022*.
\[[AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/20018)\]
\[[arXiv](http://arxiv.org/abs/2112.04840)\]
\- RM takes the rank of candidate boxes from teachers as a new form of knowledge to distill. PFI attempts to correlate feature differences with prediction differences.

- Knowledge Distillation for Object Detection via Rank Mimicking and Prediction-Guided Feature Imitation
- Gang Li and Xiang Li and Yujie Wang and Shanshan Zhang and Yichao Wu and Ding Liang

*NeurIPS 2022*.
\[[OpenReview](https://openreview.net/forum?id=O3My0RK9s_R)\]
\[[arXiv](https://arxiv.org/abs/2211.13133v1)\]
<[GitHub](https://github.com/kornia/kornia)>
\- By taking into account additional contrast and structural cues, feature importance, correlation, and spatial dependence in the feature space are considered in the loss formulation.

- Structural Knowledge Distillation for Object Detection
- Philip De Rijk and Lukas Schneider and Marius Cordts and Dariu M Gavrila

CrossKD.
\[[arXiv](https://arxiv.org/abs/2306.11369)\]
<[GitHub](https://github.com/jbwang1997/CrossKD)>
\- Delivers the intermediate features of the student's detection head to the teacher's detection head

- CrossKD: Cross-Head Knowledge Distillation for Dense Object Detection
- Jiabao Wang and Yuming Chen and Zhaohui Zheng and Xiang Li and Ming-Ming Cheng and Qibin Hou

## Knowledge Distillation for Specific Object Detectors

### Knowledge Distillation for GFL

LD. *CVPR 2022*.
\[[CVF](https://openaccess.thecvf.com/content/CVPR2022/html/Zheng_Localization_Distillation_for_Dense_Object_Detection_CVPR_2022_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9878414/)\]
\[[arXiv](http://arxiv.org/abs/2102.12252)\]
<[GitHub](https://github.com/HikariTJU/LD)>
<[MMDet](https://github.com/open-mmlab/mmdetection/tree/master/configs/ld)>
\- Standard KD by adopting the general localization representation of bounding box.

- Localization Distillation for Dense Object Detection
- Zhaohui Zheng and Rongguang Ye and Ping Wang and Jun Wang and Dongwei Ren and Wangmeng Zuo

### Knowledge Distillation for DETR

DETRDistill. *ICCV 2023*.
\[[CVF](https://openaccess.thecvf.com/content/ICCV2023/html/Chang_DETRDistill_A_Universal_Knowledge_Distillation_Framework_for_DETR-families_ICCV_2023_paper.html)\]
\[[arXiv](http://arxiv.org/abs/2211.10156)\]
\- A novel knowledge distillation dedicated to DETR-families.

- DETRDistill: A Universal Knowledge Distillation Framework for DETR-families
- Jiahao Chang and Shuo Wang and Guangkai Xu and Zehui Chen and Chenhongyi Yang and Feng Zhao

D^3^ETR.
\[[arXiv](http://arxiv.org/abs/2211.09768)\]
\- Distills knowledge in decoder predictions and attention maps from the teachers to students.

- D^3^ETR: Decoder Distillation for Detection Transformer
- Xiaokang Chen and Jiahui Chen and Yan Liu and Gang Zeng

KD-DETR.
\[[arXiv](http://arxiv.org/abs/2211.08071)\]
\- A general knowledge distillation paradigm for DETR with consistent distillation points sampling.

- Knowledge Distillation for Detection Transformer with Consistent Distillation Points Sampling
- Yu Wang and Xin Li and Shengzhao Wen and Fukui Yang and Wanping Zhang and Gang Zhang and Haocheng Feng and Junyu Han and Errui Ding

## Knowledge Distillation for Heterogeneous Object Detector Pairs

G-DetKD. *ICCV 2021*.
\[[CVF](http://openaccess.thecvf.com/content/ICCV2021/html/Yao_G-DetKD_Towards_General_Distillation_Framework_for_Object_Detectors_via_Contrastive_ICCV_2021_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/9711293/)\]
\[[arXiv](http://arxiv.org/abs/2108.07482)\]
\- A novel semantic-guided feature imitation technique, which automatically performs soft matching between feature pairs across all pyramid levels to provide the optimal guidance to the student.

- G-DetKD: Towards General Distillation Framework for Object Detectors via Contrastive and Semantic-guided Feature Imitation
- Lewei Yao and Renjie Pi and Hang Xu and Wei Zhang and Zhenguo Li and Tong Zhang

HEAD. *ECCV 2022*.
\[[ECVA](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136690310.pdf)\]
\[[Springer](https://link.springer.com/chapter/10.1007/978-3-031-20077-9_19)\]
\[[arXiv](https://arxiv.org/abs/2207.05345)\]
<[GitHub](https://github.com/LutingWang/HEAD)>
\- HEtero-Assists Distillation leveraging heterogeneous detection heads as assistants to guide the optimization of the student detector.

- HEAD: HEtero-Assists Distillation for Heterogeneous Object Detectors
- Luting Wang and Xiaojie Li and Yue Liao and Zeren Jiang and Jianlong Wu and Fei Wang and Chen Qian and Si Liu

PKD. *NeurIPS 2022*.
\[[OpenReview](https://openreview.net/forum?id=Q9dj3MzY1o7)\]
\[[arXiv](https://arxiv.org/abs/2207.02039v2)\]
<[GitHub](https://github.com/open-mmlab/mmrazor)>
\- Imitate features with Pearson Correlation Coefficient to focus on the relational information from the teacher and relax constraints on the magnitude of the features.

- PKD: General Distillation Framework for Object Detectors via Pearson Correlation Coefficient
- Weihan Cao and Yifan Zhang and Jianfei Gao and Anda Cheng and Ke Cheng and Jian Cheng

## Teacher Free Knowledge Distillation for Object Detectors

MimicDet. *ECCV 2020*.
\[[ECVA](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123590528.pdf)\]
\[[Springer](https://link.springer.com/chapter/10.1007/978-3-030-58568-6_32)\]
\[[arXiv](http://arxiv.org/abs/2009.11528)\]
\- A novel and efficient framework to train a one-stage detector by directly mimic the two-stage features, aiming to bridge the accuracy gap between one-stage and two-stage detector.

- MimicDet: Bridging the Gap Between One-Stage and Two-Stage Object Detection
- Xin Lu and Quanquan Li and Buyu Li and Junjie Yan

LabelEnc. *ECCV 2020*.
\[[ECVA](https://www.ecva.net/papers/eccv_2020/papers_ECCV/papers/123700528.pdf)\]
\[[Springer](https://link.springer.com/chapter/10.1007/978-3-030-58595-2_32)\]
\[[arXiv](http://arxiv.org/abs/2007.03282)\]
<[GitHub](https://github.com/megvii-model/LabelEnc)>
\- A new intermediate supervision method to boost the training of object detection systems.

- LabelEnc: A New Intermediate Supervision Method for Object Detection
- Miao Hao and Yitao Liu and Xiangyu Zhang and Jian Sun

HEAD. *ECCV 2022*.
\[[ECVA](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136690310.pdf)\]
\[[Springer](https://link.springer.com/chapter/10.1007/978-3-031-20077-9_19)\]
\[[arXiv](https://arxiv.org/abs/2207.05345)\]
<[GitHub](https://github.com/LutingWang/HEAD)>
\- HEtero-Assists Distillation leveraging heterogeneous detection heads as assistants to guide the optimization of the student detector.

- HEAD: HEtero-Assists Distillation for Heterogeneous Object Detectors
- Luting Wang and Xiaojie Li and Yue Liao and Zeren Jiang and Jianlong Wu and Fei Wang and Chen Qian and Si Liu

LGD. *AAAI 2022*.
\[[AAAI](https://ojs.aaai.org/index.php/AAAI/article/view/20240)\]
\[[arXiv](http://arxiv.org/abs/2109.11496)\]
\- The first self-distillation framework for general object detection.

- LGD: Label-Guided Self-Distillation for Object Detection
- Peizhen Zhang and Zijian Kang and Tong Yang and Xiangyu Zhang and Nanning Zheng and Jian Sun

SSD-Det. *ICCV 2023*.
\[[CVF](https://openaccess.thecvf.com/content/ICCV2023/html/Wu_Spatial_Self-Distillation_for_Object_Detection_with_Inaccurate_Bounding_Boxes_ICCV_2023_paper.html)\]
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/10377611)\]
\[[arXiv](http://arxiv.org/abs/2307.12101)\]
\- Mine spatial information to refine the inaccurate box in a self-distillation fashion.

- Spatial Self-Distillation for Object Detection with Inaccurate Bounding Boxes
- Di Wu and Pengfei Chen and Xuehui Yu and Guorong Li and Zhenjun Han and Jianbin Jiao

## Miscellaneous

*TPAMI*.
\[[IEEE Xplore](https://ieeexplore.ieee.org/abstract/document/10070820)\]
\- A comprehensive survey of KD-based OD models.

- When Object Detection Meets Knowledge Distillation: A Survey
- Zhihui Li and Pengfei Xu and Xiaojun Chang and Luyao Yang and Yuanyuan Zhang and Lina Yao and Xiaojiang Chen

ScaleKD. *CVPR 2023*.
\[[CVF](https://openaccess.thecvf.com/content/CVPR2023/html/Zhu_ScaleKD_Distilling_Scale-Aware_Knowledge_in_Small_Object_Detector_CVPR_2023_paper.html)\]
\- Consists of a Scale-Decoupled Feature distillation module and a Cross-Scale Assistant.

- ScaleKD: Distilling Scale-Aware Knowledge in Small Object Detector
- Yichen Zhu and Qiqi Zhou and Ning Liu and Zhiyuan Xu and Zhicai Ou and Xiaofeng Mou and Jian Tang

## Newly Published Papers
