
<img src="https://github.com/AIM3-RUC/YouMakeup/blob/master/images/logo.png" width = "500" height = "150" alt="" align=center />  


## Introduction
YouMakeup is a large-scale multimodal instructional video dataset introduced in [YouMakeup: A Large-Scale Domain-Specific Multimodal Dataset for Fine-Grained Semantic Comprehension](https://www.aclweb.org/anthology/D19-1517/) (*EMNLP2019*). 

It contains 2,800 videos from YouTube, spanning more than 420 hours in total. Each video is annotated with a sequence of steps, including temporal boundaries, grounded facial areas and natural language descriptions of each step.

![image](https://github.com/AIM3-RUC/YouMakeup/blob/master/images/annotation.png)


Makeup activities are fine-grained in nature. Different makeup steps share the same facial background but contain at least one subtle but critical difference in action, tool, product or facial area. Therefore, it requires fine-grained discrimination within temporal and spatial context to distinguish them. Our YouMakeup dataset can support various tasks for fine-grained semantic comprehension.

![image](https://github.com/AIM3-RUC/YouMakeup/blob/master/images/comparison.png)

## CVPR 2020 Workshop: YouMakeup VQA chanllenge

We propose two video question answering tasks in the CVPR 2020 workshop ***Language & Vision with applications to Video Understanding***. The details of the chanllenge are introduced in [CVPR_2020_YouMakeup_VQA_chanllenge](https://languageandvision.github.io/youmakeup_vqa/index.html).

#### Facial Image Ordering

As instructional video present steps for accomplishing a certain task, tracking the changes of object after the steps is crucial for procedure understanding. The effects of makeup are fine-grained changes of facial appearances. Therefore, we propose the facial image ordering task, which is to sort a set of facial images from a video into the correct order according to the given step descriptions.

![image](https://github.com/AIM3-RUC/YouMakeup/blob/master/images/image_ordering.png)

#### Step Ordering

Cross-model semantic alignment is important in the field of visual and language. In the step ordering task, we ask models to sort a set of step descriptions into the right order as these actions are performed in the video. Models need to align textual step descriptions with corresponding video contents to solve the task. Since the makeup videos contain a sequence of actions and texts are composed of multi-sentences, the task also requires long-term temporal action reasoning and text understanding.

![image](https://github.com/AIM3-RUC/YouMakeup/blob/master/images/step_ordering.png)

### Data Download
The data license form should be signed before accessing the data. Please sign the form
```
data/Liscense Agreement.pdf
```
and send it to youmakeupvqa@163.com and we will provide the link for data download.



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

If you have any questions about YouMakeup dataset, please contact us by wy.wang@ruc.edu.cn.

If you have any questions about the YouMakeup VQA chanllenge, please contact us by youmakeupvqa@163.com 
