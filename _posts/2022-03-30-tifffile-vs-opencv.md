---
layout: post
title: Tifffile vs Opencv in Python
date: 2022-03-30
description: Beware the difference between `cv2.imread` and `tifffile.imread` in Python
disqus_comments: true
tags: python, image_processing
---

If you're using opencv and/or tifffile to prepare your dataset for training deep learning models, beware the difference between the imread function in both libraries, i.e., `cv2.imread` and `tifffile.imread`. It makes a huge difference, especially if you have custom, multi-channel images. 

Let's experiment with an example custom tif image with dimensions 224x224x4 below.


```python
# import necessary modules

import cv2
import tifffile
import matplotlib.pyplot as plt
%matplotlib inline


# read image with tifffile

image_tifffile = tifffile.imread('example.tif')
print(image_tifffile.shape) # prints 224x224x4

```

    (224, 224, 4)




```python
# read image with cv2
image_cv2 = cv2.imread('example.tif', cv2.IMREAD_UNCHANGED)
print(image_cv2.shape) # also prints 224x224x4
```

    (224, 224, 4)


Looks great, the same image read with both libraries are read and have the same size. However, there is a twist. Let's use `matplotlib` and plot all four slices for the image read by both libraries.


```python
# plot all four slices for both images read above
fig, ax = plt.subplots(2, 4)
for i in range(4):
    ax[0, i].imshow(image_tifffile[:,:,i], cmap='gray')
    ax[1, i].imshow(image_cv2[:,:,i], cmap='gray')
for axi in ax.ravel():
    axi.set_axis_off()

plt.show()
```



<div class="row mt-3">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/output_4_0.png" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>

    


The first row shows the four slices for the image read with tifffile. The second row shows the same, but read with opencv (cv2)

Opencv swaps channels 1 and 3. I learned it the hard way, and wanted to give you a heads-up! I hope you enjoyed reading.

Cheers :)




