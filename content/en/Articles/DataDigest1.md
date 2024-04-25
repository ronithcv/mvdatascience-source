---
author: ""
title: "Data Digest 1"
date: 2023-11-13
description: "Issue 1: Diffusion Models and Applications"
tags: ["shortcodes", "privacy"]
thumbnail: "/DataDigest1.png"
displayShort: false
---
Diffusion Models are a class of generative models that turn noise into a
data sample. The goal of a diffusion model is to decode the noise of an
image.

From the authors of the first paper on diffusion they state: “The
essential idea is to systematically and slowly destroy data in a data
distribution through an iterative forward process. We then learn a
reverse diffusion process that restores structure in data,".

What this is saying is that first we randomly add noise to a picture
little by little, and then we use a diffusion model to reverse this
process, decoding the noise little by little, until we have the final
image.

![Placeholder](/Img1.png)

Timesteps of adding noise to an image, until its pure noise. Sampled
from the normal distribution z ~ N(0, 1).

Now the network has to learn to remove noise step by step from the
image, until it's removed all of it. This is done using a U-net, which
first downsamples the image, denoises it and then upscales the image.
Attention blocks are put between layers with the same resolution. To
tell which timestep the picture is in, we utilize embeddings.

Iterative process of denoising an image using a diffusion model

![Placeholder](/Img2.png)
![Placeholder](/Img3.png)

U-net architecture

The applications are endless and include image denoising, inpainting (filling in or removing objects in pictures), super resolution (increasing resolution of an image), and Image Generation.

<b>Resources: </b>

https://en.wikipedia.org/wiki/Diffusion_model

Video: https://www.youtube.com/watch?v=TBCRlnwJtZU 

Research Papers: https://arxiv.org/abs/1503.03585 https://arxiv.org/abs/2105.05233

Learn More: https://www.youtube.com/watch?v=sFztPP9qPRc
