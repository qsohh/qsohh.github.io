---
title: "Stereo Vision for Obstacle and Lane Detection"
permalink: /projects/stereovision/
layout: single
author_profile: true
---

This project implements a pipeline for obstacle and lane marking detection from stereo camera input, using traditional computer vision methods such as disparity estimation, edge detection, and Hough transforms.

---

## Project Goals

Detect lane markings and obstacles using stereo vision, disparity maps, and geometric reasoning — **without deep learning**.

---

## Input stereo images

<div style="display: flex; gap: 10px;">
  <img src="/assets/images/projects_MIV308/01G.png" width="45%">
  <img src="/assets/images/projects_MIV308/01D.png" width="45%">
</div>

> Initial stereo image pair (left and right views).

---

## Main Processing steps

- Applied morphological filtering and edge detection to extract structural features.
  - Lane markings were further isolated by subtracting a low-pass filtered version of the image (using a rectangular average filter), which enhanced **horizontal high-frequency components**. This helped distinguish lane markings from vehicles or other low-frequency features.
- Constructed a vertical disparity map (`v-disparity`) to identify the road plane and detect vertical features above it.
- Performed Hough transform in v-disparity space to extract dominant straight lines.
  - Two key lines in this space represent the set of lane boundaries and the elevated structure (i.e., the vehicle in our scene).

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
  <img src="/assets/images/projects_MIV308/gd_ouvert.jpg" width="64%">
  <img src="/assets/images/projects_MIV308/v_dis.jpg" width="9%">
  <img src="/assets/images/projects_MIV308/hough.jpg" width="9%">
</div>

> Detected edges, v-disparity map, and Hough line detection.

---

## Colored disparity map

<img src="/assets/images/projects_MIV308/color_disp.jpg" width="45%">

> Pixel color: red -> blue corresponds to near -> far depth.

---

## Final results

<img src="/assets/images/projects_MIV308/result.jpg" width="45%">

> Scene segmentation: red = lane markings, yellow = road, blue = occupied area, green = detected obstacle.

---

## Tools Used

- **Matlab**: implemented the entire detection pipeline using image processing toolbox and custom stereo geometry code.
