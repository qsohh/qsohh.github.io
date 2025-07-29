---
title: "Projects"
permalink: /projects/
layout: single
author_profile: true
---

### Real-time Crypto Trading Bot

- Built a modular bot with signal-based strategy and live execution (backtested and deployed on Binance test net)
- Integrated WebSocket event listener and real-time volume/price signals
- Strategy tuning via PyTorch (parameter optimization ongoing)
- [GitHub repo](https://github.com/qsohh/Binance_Trade)

---

### Survival Modeling with DeepSurv (QRT Challenge)

- Modeled patient survival using linear CoxPH (sksurv) model and a PyTorch-based nonlinear DeepSurv model
- Focused on censored data handling, model interpretability and calibration
- [GitHub repo](https://github.com/qsohh/Challenge_Data_QRT)

---

### Image processing - Obstacle and Road Marking Detection via Classical Stereo Vision

This student project implemented a classical computer vision pipeline for detecting obstacles and lane markings using stereo image pairs and disparity maps.

**Main steps included:**

- Preprocessing stereo images using morphological filtering and edge detection.
- Constructing v-disparity and Hough space representations to identify dominant planes and lane structures.
- Estimating the road area and detecting obstacles through geometric reasoning based on disparity and color segmentation.

<img src="/assets/images/projects_MIV308/01G.png" width="30%" alt="left image">

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
  <img src="/assets/images/projects_MIV308/01G.png" width="30%" alt="left image">
  <img src="/assets/images/projects_MIV308/01D.png" width="30%" alt="right image">
  <img src="/assets/images/projects_MIV308/result.jpg" width="30%" alt="result">
</div>

[View detailed vision demo](/projects/stereovision/)

---

### Ray tracing