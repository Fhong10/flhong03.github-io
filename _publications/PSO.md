---
title: "Particle Swarm Optimization"
collection: publications
permalink: /research/project-4/
excerpt: "Extracting Anisotropic Extinction Coeffcients."
---

### Motivation

Absorption values of UV-Vis spectroscopy only generate extinction coefficients in-plane components. Therefore, I tried to find extinction coefficients based on mean-squared error between theoretical graphs and experimental data graphs. Once I input optical parameters, algorithm finds the minimum value and display the optical parameters such as extinction coefficients on the screen. TO find minimum mean squared values, I used the grid search and particle swarm optimizaiton.


## Grid search

I initially used the grid search in Python. Theoretical refletivity is plotted using parameter such as thickness of each materials, refractive index etc. Each plotted reflectivity is subtracted from measured reflectivity data and find the minimum value. Based on number of parameters vector space, it consumes a lot of time to compute the optimized refractive index.

## Particle Swarm Optimization

I implemented particle swarm optimization in MATLAB to reduce time. 
 




