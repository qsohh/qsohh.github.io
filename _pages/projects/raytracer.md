---
title: "Ray Tracer in Python and Rust"
permalink: /projects/raytracer/
layout: single
author_profile: true
---

This project implements a basic ray tracer from scratch in Python, later reimplemented in Rust for significant performance improvement. It renders spheres and triangles using the Phong illumination model, supporting shadows and recursive reflections.

---

## Introduction

<img src="/assets/images/projects_IN104/intro.jpg" width="90%">

> A simple illustration of how ray tracing works compared to natural vision.

---

## Features

- Ray-object intersection (spheres and triangles)
- Phong illumination (ambient, diffuse, specular)
- Shadow ray casting
- Recursive reflections (mirror effects)
- Refraction can be implemented easily by extending the reflection model
- Parallel rendering using CPU cores
- Rust implementation for performance optimization

---

## Core Algorithm Steps

1. Cast a view ray for each pixel  
2. Find the closest intersection with scene objects  
3. Compute local color using:
   - Surface normal
   - Light position
   - Shadow ray
   - Reflection
4. If the material is reflective, compute reflected ray color recursively

---

## Sample Renderings

<div style="display: flex; gap: 10px;">
  <img src="/assets/images/projects_IN104/two_spheres.png" width="45%">
  <img src="/assets/images/projects_IN104/cover_render.jpg" width="45%">
</div>

> Left: reflections and shadows between two colored spheres  
> Right: super HD sample with random spheres at random positions

---

## Tools Used

- **Python**: initial version, `multiprocessing` for parallel rendering
- **Rust**: optimized version

---

[Back to Projects](/projects/)