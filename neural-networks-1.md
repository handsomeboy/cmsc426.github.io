---
layout: page
permalink: /pano/
---

Table of Contents:

- [Quick intro without brain analogies](#quick)
- [Modeling one neuron](#intro)
  - [Biological motivation and connections](#bio)
  - [Single neuron as a linear classifier](#classifier)
  - [Commonly used activation functions](#actfun)
- [Neural Network architectures](#nn)
  - [Layer-wise organization](#layers)
  - [Example feed-forward computation](#feedforward)
  - [Representational power](#power)
  - [Setting number of layers and their sizes](#arch)
- [Summary](#summary)
- [Additional references](#add)

<a name='quick'></a>
# Introduction:




## Convolution:
- 1D Conv
- 2D and 3D Conv
- Conv in images
- Deconvolution
- Optional read [Fourier Transform]

## 
- Point operators
- Filtering (`imfilter` and `imgaussfilt`) (MEAN, MEDIAN filters)
- Sobel, Prewitt filtering
- Padding in images (`paddarray`)
- Erosion and Dilation (`imerode` and `imdilate`)
- Denoising

## Features Detection:
- What are features?
- Derivates in images
- Edge: Canny `approxcanny` , Sobel, Prewitt, Roberts.
- Corner: Harris, Shi Tomasi, FAST
- Blob detection: LoG, DoG
- Feature Descriptor: SIFT (Scale selectivity (CIS 580) Multi-scale concepts), SURF and HOG


## Camera Model
- Pinhole model
- Distortion
- Intrinsic Calibration $$K$$ Matrix
- Extrinsic calibration (couple of lines)


## Transformation:
- Homogenous Coordinates
- Projective Geometry
- Projective Transformation
- Affine Tranformation
- Vanishing Points
- Homography
- Deep learning, CNN and Deep Homography
- Single View Geometry

## Panorama Stitching:
- ANMS
- Feature Correspondence
- Homography
- Make it robust using RANSAC
- Cylindrical Projection
- Blending images (Laplacian Pyramid)
- 






<div class="fig figcenter fighighlight">
  <img src="/assets/nn1/neuron.png" width="49%">
  <img src="/assets/nn1/neuron_model.jpeg" width="49%" style="border-left: 1px solid black;">
  <div class="figcaption">A cartoon drawing of a biological neuron (left) and its mathematical model (right).</div>
</div>


<a name='add'></a>

## Additional References

- [deeplearning.net tutorial](http://www.deeplearning.net/tutorial/mlp.html) with Theano
- [ConvNetJS](http://cs.stanford.edu/people/karpathy/convnetjs/) demos for intuitions
- [Michael Nielsen's](http://neuralnetworksanddeeplearning.com/chap1.html) tutorials
