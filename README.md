# YouMakeup Dataset
## Introduction
YouMakeup is a large-scale multimodal instructional video dataset introduced in [YouMakeup: A Large-Scale Domain-Specific Multimodal Dataset for Fine-Grained Semantic Comprehension](https://www.aclweb.org/anthology/D19-1517/) (*EMNLP2019*).

It contains 2,800 videos from YouTube, spanning more than 420 hours in total. Each video is annotated with a sequence of steps, including temporal boundaries, grounded facial areas and natural language descriptions of each step.

![image](https://github.com/AIM3-RUC/YouMakeup/blob/master/images/annotation.png)


Makeup activities are fine-grained in nature. Different makeup steps share the same facial background but contain at least one subtle but critical difference in action, tool, product or facial area. Therefore, it requires fine-grained discrimination within temporal and spatial context to distinguish them. Our YouMakeup dataset can support various tasks for fine-grained semantic comprehension.

![image](https://github.com/AIM3-RUC/YouMakeup/blob/master/images/comparison.png)

## Task

#### Facial Image Ordering

The facial image ordering task is to sort a series of shuffled facial images into the right order according to the ordered step captions. The effect of makeup is the fine-grained changes of facial appearances. Tracking changes on the face is an effective way to evaluate fine-grained comprehension ability.

![image](https://github.com/AIM3-RUC/YouMakeup/blob/master/images/image_ordering.png)

#### Step Ordering

The step ordering task evaluates the capability of sorting a series of step captions into the right order according to the video. This task aims at developing model’s comprehension ability in a multimodal scenario, which calls for a joint understanding across different modalities.

![image](https://github.com/AIM3-RUC/YouMakeup/blob/master/images/step_ordering.png)

##### These two tasks will be part of the chanllenge tasks for CVPR 2020 workshop ***Language & Vision with applications to Video Understanding***

## Citation

```
@inproceedings{wang2019youmakeup,
  title={YouMakeup: A Large-Scale Domain-Specific Multimodal Dataset for Fine-Grained Semantic Comprehension},
  author={Wang, Weiying and Wang, Yongcheng and Chen, Shizhe and Jin, Qin},
  booktitle={Proceedings of the 2019 Conference on Empirical Methods in Natural Language Processing and the 9th International Joint Conference on Natural Language Processing (EMNLP-IJCNLP)},
  pages={5136--5146},
  year={2019}
}
```

If you have any questions, please contact us by wy.wang@ruc.edu.cn
