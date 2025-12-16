---
title: "Particle Swarm Optimization"
collection: publications
permalink: /research/project-4/
excerpt: "Extracting Anisotropic Extinction Coeffcients."
---

### Motivation

UV-Vis spectroscopy probes optical absorption with the elctric field oscillating parallel to the film surface, yielding extinction coefficients corresponding only to in-plane optical response. However, accurate modeling of multilayer reflectivity requires both in-plane and out-of-plane extinction coefficients. To address this limitation, I formulated an inverse problem in which anisotropic extinction coefficients were extracted by minimizing the mean-squared error between theoretically calculated and experimentally measured reflectivity spectra.

Given a set of optical parameters, the algorithm computes theoretical reflectivity curves and iteratively searches for parameter values that minimize the discrepancy with experimental data. The optimized extinction coefficients are then returned as the output.

## Grid search

<img src="{{ '/images/gridsearch.gif' | relative_url }}"
     alt="PSO visulaization"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

 I first implemented a grid search in Python: reflectivity spectra are computed with the Transfer Matrix Method with optical parameters. If we fix these parameters, the mean squared errors (MSE) between theoretical reflectivity and measured reflectivity at each (n,k) is calculated. In the visualization, a white cursor walks the grid as each point is evaluated, and a red marker tracks the current best (lowest) MSE. However, the  computational time increased rapidly with the dimensionality of the parameter space, even exceeding 3 hours
 
Grid search yields corresponding result: 

 <img src="{{ '/images/gridresult.png' | relative_url }}"
     alt="PSO visulaization"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">


## Particle Swarm Optimization(PSO)

<img src="{{ '/images/PSOgif2.gif' | relative_url }}"
     alt="PSO visulaization"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

To reduce the computational time of grid search, I implemented particle swarm optimization (PSO) in MATLAB. PSO efficiently explores the parameter space by evolving a population of candidate solutions based on both individual and collective optimization behavior.

Using PSO, anisotropic extinction coefficients were extracted by minimizing the mean-squared error between simulated and experimental reflectivity spectra with significantly reduced computation time. This approach enabled efficient and robust fitting of optical parameters in anisotropic multilayer systems.

<div class="pso-explainer" style="line-height: 1.35;">
  <p style="margin: 0 0 8px 0;">The plot is a Particle Swarm Optimization (PSO) run on two parameters (n and k). Each white dot is a particle position; the red dot marks the global best candidate found; the yellow star marks the final selected solution. Iteration is 40 to find a best mean squared error (MSE) of 5.896×10⁻⁴.</p>
  <p style="margin: 0 0 8px 0;">Color map: It encodes log10(MSE) of the objective over the (n, k) plane.</p>
  <p style="margin: 0 0 8px 0;">Blue/purple = lower MSE (better fit).</p>
  <p style="margin: 0 0 8px 0;">Yellow = higher MSE (worse fit).</p>
  <p style="margin: 0;">The color bar spans roughly −3 to −1, so MSE ranges from about 10⁻³ to 10⁻¹ across the plotted region.</p>
</div>

## The result

Both optimization methods yielded the same optimized parameters, while particle swarm optimization significantly reduced computation time compared to grid search.

