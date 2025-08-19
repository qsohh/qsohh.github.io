---
title: "Projects"
permalink: /projects/
layout: single
author_profile: true
---

### Q_Trader – Modular Execution Framework for Binance

- Developed a lightweight trading framework focusing on the execution layer (order placement, balance management, market data retrieval)  
- Designed a plug-in interface for strategies via a factory pattern, allowing seamless switch between demo and proprietary strategies  
- Live trading loop supports both Binance Testnet and mainnet, with history logging and periodic strategy re-initialization  
- Proprietary strategies include adaptive weight models trained with **PyTorch**, which remain private  
- Released under MIT License (executor open-sourced, proprietary strategies kept private)

> [GitHub repo](https://github.com/qsohh/Q_Trader)

---

### Quommoty – Futures Pricer (QuantLib-based)

A prototype futures pricing framework built in C++ with [QuantLib](https://www.quantlib.org/). Implements a shared pricing interface and specialized pricers for crude oil (cost-of-carry model) and electricity (forward-anchor with delivery averaging).

This is an iterative prototype project, primarily for personal learning and practice.

- Focus: commodity futures pricing models (storable vs. non-storable commodities)
- Includes demo tests and modular design for extension

> [GitHub repo](https://github.com/qsohh/Quommoty)

---

### Survival Modeling with DeepSurv (QRT Challenge)

- Modeled patient survival using linear CoxPH (sksurv) model and a PyTorch-based nonlinear DeepSurv model
- Focused on censored data handling, model interpretability and calibration

> [GitHub repo](https://github.com/qsohh/Challenge_Data_QRT)

---

### Image processing - Obstacle and Road Marking Detection via Classical Stereo Vision

This project implements a pipeline for obstacle and lane marking detection from stereo camera input, using traditional computer vision methods such as disparity estimation, edge detection, and Hough transforms.

<div style="display: flex; flex-wrap: wrap; gap: 10px;">
  <img src="/assets/images/projects_MIV308/01G.png" width="30%" alt="left image">
  <img src="/assets/images/projects_MIV308/01D.png" width="30%" alt="right image">
  <img src="/assets/images/projects_MIV308/result.jpg" width="30%" alt="result">
</div>

> [View full project](/projects/stereovision/)

---

### Ray Tracer

<img src="/assets/images/projects_IN104/cover_render.jpg" width="60%">

> Realistic rendering with reflection and shadows using recursive ray tracing.  
> [View full project](/projects/raytracer/)

---

### Petit Metro Simulator

Simulates train behavior under CBTC-based signaling systems, modeling tracks, signals, and station control.  
Includes extensible train dynamic modules, train control system logic, and visualization of simulation results.

<img src="/assets/images/projects_railway_signaling_simulator/ex_simulation.png" width="40%">

> Below is a sample output showing a train adapting to speed limits and signal targets along the track.  
> [View full project](/projects/railway_signaling_simulator)  
> [GitHub repo](https://github.com/qsohh/PetitMetroHao)
