---
layout: page
title: Driver alert system
description: Using CV to keep drivers safe
img: /assets/img/Jetson.jpg
---

This is a project which I am working on with [Jada Flanagan](https://www.linkedin.com/in/jada-flanagan-5b6866153/) and it's still in its early stages. The basic idea is to leverage the recent advances in computer vsion and edge computing to create a retrofit kit which can be placed in a car to alert the driver to dangerous situations on the road. This device would have a forward looking camera, mounted either in the grille or secured to the dashboard, and would alert the driver to threats with some combination of light and sound. Some initial tasks I would like to accomplish are detecting when the car is leaving the lane, when there is a pedestrian entering the road, or when when the driver is too close to a car in front. 

I have purchased a NVIDIA Jetson TX2 and plan to begin doing more work over winter break. It seems that simple geometric vision techniques such as color-based segmentation and the Hough transform can be used to extract the lines with fairly high accuracy. This means that the first task should be fairly simple and run easily in real-time. The latter two tasks could be accomplishes with any one of a number of deep convoltional neural networks, such as [Mask R-CNN](https://github.com/facebookresearch/Detectron) or [Mobilenent](https://github.com/tensorflow/models/blob/master/research/slim/nets/mobilenet_v1.md). Because of the computational constrainsts, it is likely we will have to make some tradeoffs between framerate and accuracy. However, given reasonably-good detections, it should be possible to understand whether the objects are in the lane and if they pose a threat.

