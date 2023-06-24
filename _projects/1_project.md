---
layout: page
title: spatial-kfold #<h1>Spatial-kfold</h1>
description: A Python Package for Spatial Resampling Toward More Reliable Cross-Validation in Spatial Studies. 
img: assets/img/projects/project_1/trees.jpg
importance: 1
category: Open Source
---

## Source code
🔗 [spatial-kfold](https://github.com/WalidGharianiEAGLE/spatial-kfold)

## Motivations

During my MSc thesis, I developed a Python package aimed at enhancing the reliability of cross-validation for spatial data. There seems to be a misconception regarding the appropriate choice of cross-validation strategy when conducting spatial predictions and evaluating machine learning algorithms. Many researchers often opt for random cross-validation or k-fold techniques, which fail to consider the spatial nature of the data and the presence of spatial autocorrelation [Bahn & McGill, 2012](https://doi.org/10.1111/ecog.02881). Consequently, this approach may lead to an overly optimistic assessment of the model's performance and an overfitting issue. This is why I created this package, to address not only the issue of overfitting but also to provide a more reliable evaluation of model performance.

## Description

spatial-kfold is a python library for performing spatial resampling to ensure more robust cross-validation in spatial studies. It offers spatial clustering and block resampling techniques with user-friendly parameters to customize the resampling. It enables users to conduct a "Leave Region Out" cross-validation, which can be useful for evaluating the model's generalization to new locations as well as improving the reliability of feature selection [Meyer et al., 2019](https://doi.org/10.1016/j.ecolmodel.2019.108815) and hyperparameter tuning [Schratz et al., 2019](https://doi.org/10.1016/j.ecolmodel.2019.06.002) in spatial studies.


## Main Features

spatial-kfold allow to conduct "Leave Region Out" using two spatial resampling techniques:

* 1- Spatial clustering with kmeans
* 2- Spatial blocks
    * Random blocks
    * Continuous blocks 
        * tb-lr : top-bottom, left-right
        * bt-rl : bottom-top, right-left

## Installation

spatial-kfold can be installed from [PyPI](https://pypi.org/project/spatial-kfold/)

```py
pip install spatial-kfold
```
### Spatial resampling

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/project_1/blocks_resampling
.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    Spatially Clustered Folds.
</div>

### Random and Spatial cross validation

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/projects/project_1/randomCV_spatialCV.png" title="example image" class="img-fluid rounded z-depth-1" zoomable=true %}
    </div>
</div>
<div class="caption">
    k-fold vs spatial-kfold.
</div>

    ---
    Background image srource: Photo by Lukasz Szmigiel on Unsplash 
    ---