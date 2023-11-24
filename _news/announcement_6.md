---
layout: post
title: Prize Winning Solution at the Help a hematologist out Challenge 
date: 2022-09-23
inline: false
disqus_comments: true
---

We placed 3rd in the Help a hematologist out Challenge at the Helmholtz Incubator Summer Academy – From Zero to Hero, 2022.


I attended the Helmholtz Incubator Summer Academy - From Zero to Hero, 2022. I specially took part in the [Help a hematologist out Challenge](https://helmholtz-data-challenges.de/web/challenges/challenge-page/93/overview){:target="_blank"} and joined the BLAMAD team. The theme of the challenge was to find creative domain adaptation solutions for blood-cell classification which is important for diagnosis of diseaeses such as anemia or leukemia. 

We were given two annotated datasets (Mat_19 and Ace_20) on white blood cell images and the goal was to classify the cell type on a third, unseen dataset (WBC1). We used Cycle-GAN for domain adaptation, i.e., unpaird image translation between images in the annotated datasets and images in the unseen dataset. Afterwards, the trained generator was used to transform images in the annotated datasets to those of the unseen dataset. An example image-to-image translation between source and target datasets is shown below:



<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/hematologist.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Example source <---> target translation using Cycle-GAN
</div>




A [resnet18](https://pytorch.org/vision/main/models/generated/torchvision.models.resnet18.html){:target="_blank"} classifier was trained on the newly transformed annotated dataset and applied on the unseen dev set. We placed 5th on the dev phase of the challenge as shown below:


<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/devphase.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
Dev Phase Leaderboard
</div>


Luckily, our model was good in generalization and hence, we placed 3rd at the test phase and each of us won a power bank at the award ceremony :)


<div class="row mt-2">
    <div class="col-sm mt-2 mt-md-0">
        {% include figure.html path="assets/img/testphase.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Test Phase Leaderboard
</div>

The code and detailed information on the whole challenge is available [here](https://github.com/Bashirkazimi/Help-a-hematologist-out-Challenge){:target="_blank"}.

I would like to thank the organizers of the challenge and my BLAMAD teammates: Bashir (Me), Lea Gabele, Ankita Negi, Martin Brenzke, Arnab Majumdar, and Dawit Hailu.


## References

```
@inproceedings{CycleGAN2017,
  title={Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks},
  author={Zhu, Jun-Yan and Park, Taesung and Isola, Phillip and Efros, Alexei A},
  booktitle={Computer Vision (ICCV), 2017 IEEE International Conference on},
  year={2017}
}


@inproceedings{isola2017image,
  title={Image-to-Image Translation with Conditional Adversarial Networks},
  author={Isola, Phillip and Zhu, Jun-Yan and Zhou, Tinghui and Efros, Alexei A},
  booktitle={Computer Vision and Pattern Recognition (CVPR), 2017 IEEE Conference on},
  year={2017}
}

@misc{cyclegan,
  author = {Jun-Yan Zhu},
  title = {CycleGAN and pix2pix in PyTorch},
  year = {2017},
  publisher = {GitHub},
  journal = {GitHub repository},
  howpublished = {\url{https://github.com/junyanz/pytorch-CycleGAN-and-pix2pix}}
}

@inproceedings{he2016deep,
  title={Deep residual learning for image recognition},
  author={He, Kaiming and Zhang, Xiangyu and Ren, Shaoqing and Sun, Jian},
  booktitle={Proceedings of the IEEE conference on computer vision and pattern recognition},
  pages={770--778},
  year={2016}
}
```