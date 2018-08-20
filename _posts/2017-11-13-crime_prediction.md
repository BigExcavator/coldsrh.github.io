---
published: true
title: Crime Prediction based on the Video prediction model
category: Machine Learning  
tags: [Machine Learning, Python, Algorithm]
layout: post
---

# Introduction

Recently I'm doing something related to crime prediction. The task is to predict in which area inside the Chaoyang district the crime may happen.
I came up with the idea to display all the blocks in Chaoyang District as pixels on a picture, and use the brightness of each pixel to represent whether there is a crime or not in that district.

Then the whole work could be translated to a video prediction task, using the last 20 day's image to predict the 21th day's image. So a paper came into my mind:

Unsupervised Learning for Physical Interaction through Video Prediction

And the model inside it is really appropriate for my task.

# Model structure and mechanism

The model is an action-conditioned video prediction model that explicitly models pixel motion, by predicting a distribution over pixel motion from previous frames. There are three motion prediction modules presented and evaluated. The first, which we refer to as dynamic neural advection (DNA), outputs a distribution over locations in the previous frame for each pixel in the new frame. The predicted pixel value is then computed as an expectation under this distribution. A variant on this approach, which we call convolutional dynamic neural advection (CDNA), outputs the parameters of multiple normalized convolution kernels to apply to the previous image to compute new pixel values. The last approach, which we call spatial transformer predictors (STP), outputs the parameters of multiple affine transformations to apply to the previous image, akin to the spatial transformer network previously proposed for supervised learning. In the case of the latter two methods, each predicted transformation is meant to handle separate objects. To combine the predictions into a single image, the model also predicts a compositing mask over each of the transformations. DNA and CDNA are simpler and easier to implement than STP, and while all models achieve comparable performance, the object-centric CDNA and STP models also provide interpretable internal representations. 

The model's main contribution is a method for making long-range predictions in real-world videos by predicting pixel motion, which could be used in my project.

The following is the structure of the model:
![0](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23CP/0.jpg)

Architecture of the CDNA model, one of the three proposed pixel advection models. We use convolutional LSTMs to process the image, outputting 10 normalized transformation kernels from the smallest middle layer of the network and an 11-channel compositing mask from the last layer (including 1 channel for static background). The kernels are applied to transform the previous image into 10 different transformed images, which are then composited according to the masks. The masks sum to 1 at each pixel due to a channel-wise softmax. Yellow arrows denote skip connections.

# The model's perfermance

![1](https://raw.githubusercontent.com/BigExcavator/coldsrh233.github.io/master/_posts/image/%23CP/1.jpg)

The last frame is the predicated one. As we can see, the model's perfermance is acceptable.

# Model transplantation

As we can see, in the paper, the model is used to predict the mechanical arm's movement. That kind of movement has a tendency inside it, and it is similar with the crime tendency inside one city. Based on that, we tried to use this model to solve the crime prediciton work.

The model we finally used is similar with the old one, just with some parameter changed. As the result, the generated image can hit 73.3% crimes that real happened.

# Related technologies
LSTM, RNN, Video Prediciton




