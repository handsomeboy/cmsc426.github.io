---
layout: page
permalink: /panorama-stitch/
---

Table of Contents:

- [Introduction](#intro)
- [Visualizing the loss function](#vis)
- [Optimization](#optimization)
  - [Strategy #1: Random Search](#opt1)
  - [Strategy #2: Random Local Search](#opt2)
  - [Strategy #3: Following the gradient](#opt3)
- [Computing the gradient](#gradcompute)
  - [Numerically with finite differences](#numerical)
  - [Analytically with calculus](#analytic)
- [Gradient descent](#gd)
- [Summary](#summary)

<a name='intro'></a>

### Introduction


### Features in an image
What are <i>features</i> for Machine vision? <i> Is it similar as Human visual perception? This question can have different answers but one thing is certain that feature detection is an imperative building block for a variety of computer vision applications. We all have seen <i> Panorama Stitching </i> in our smartphones or other softwares like Adobe Photoshop or AutoPano Pro. The fundamental idea in such softwares is to align two or more images before seamlessly stitching into a panorama image. Now back to the question, <i> what kind of features should be detected before the alignment? </i> Can you think of a few types of features?

A set of particular position in the images like building corners or mountain peaks can be considered as features. These kinds of localized features are known as <i>corners</i> or keypoints or interest points and are widely used in different applications. These are characterized by the appearance of neigborhood pixels surrounding the point (or local patches). The other kind of feature is based on the orientation and local appearance and is generally of a good indicator of object boundaries and occlusion events. <i> Occlusion means that there is something in the field of view of the camera but due to some sensor/optical property or some other scenario, you can't.</i> 

There are multiple ways to detect certain features. One of them is convolution. <i> What is convolution? It is really 'convoluted'? </i> Before we really understand what convolution really means, think it as an operation of changing the pixel values to a new set of values based on the values of the nearby pixels. <i> Didn't get the gist of it? Don't worry! </i>

Convolution is an operation between two functions, resulting in the another function that depicts how the shape of first function is modified by the second function. The convolution of two functions, say $f$ and $g$ is written is $f\star g$ or $f*g$ and is defined as:
$$
(f*g)(t) = \int_{-\inf}{\inf} f(\tau)g(t-\tau)d\tau = \int_{-\inf}{\inf} f(t-\tau)g(\tau)d\tau
$$

The following image depcits the convolution <i>(in black)</i> of the two functions <i>(red and green).</i> One can think convolution as the common under (between $f$ and $g$) 




<a name='intro'></a>
## Camera Optics
We learned about ISO, shutter speed, apertures and focal length in the [Color Segmentation](https://cmsc426.github.io/colorseg/#colimaging) project. Let us now learn about how the camera system work! We have learned that smaller the Field Of View (FOV), larger the focal length (f) is. One can say:
$$FOV = tan^{-1}\left(\dfrac{d}{2f}\right)$$
where $$d$$ is sensor size. Figure [focal length] shows the effect of focal length to the FOV. And clearly, larger the focal length, the more _zoomed-in_ image is captured. Also, large focal length compresses the depth. Fig [imagesatdifferentF] and [depth-of-field] illustrates images captured at different focal length and their effects.

Lens distortion....

## Camera Model
