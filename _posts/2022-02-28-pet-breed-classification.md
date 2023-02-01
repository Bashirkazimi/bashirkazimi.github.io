---
layout: post
title: Pet breed classification
date: 2022-02-28
description: Saw a cute dog or a beautiful cat and wonder what breed it is? This CNN model can help you.
disqus_comments: true
tags: cnn, deep_learning
---


Oxford cats and dogs [dataset](https://www.kaggle.com/zippyz/cats-and-dogs-breeds-classification-oxford-dataset){:target="_blank"} includes images of cats and dogs and annotations for their corresponding breeds. 

I used the [ResNet](https://arxiv.org/abs/1512.03385){:target="_blank"} model in [PyTorch](https://pytorch.org/vision/stable/models.html#torchvision.models.resnet18){:target="_blank"}, pretrained on the [ImageNet](https://www.image-net.org/){:target="_blank"} dataset, and fintuned it to train a pet breed classifier. The web app is deployed [here](https://share.streamlit.io/bashirkazimi/pet-breed-classification/app.py){:target="_blank"} using [Streamlit](https://streamlit.io/){:target="_blank"}.

Check out the [repository](https://github.com/Bashirkazimi/pet-breed-classification){:target="_blank"} on GitHub or test the deployed web app and find out the breed for a pet you liked.

Please let me know if you see any mistakes or have any questions/suggestions. You could also follow me on [Twitter](https://twitter.com/bashir_kazimi){:target="_blank"} and [LinkedIn](https://www.linkedin.com/in/bashirkazimi/){:target="_blank"}.

Thanks for reading!