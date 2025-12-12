---
title: "Reflectivity Modeling of PEDOT:PSS Multilayer Devices Using Transfer Matrix Method"
collection: publications
permalink: /research/project-1/
excerpt: "Benchmarking my Python TMM solver against standard textbook results."
date: 2024-01-01
---

## Motivation
Neural recording requires resolving voltage changes as small as 10 µV. By modeling how applied voltage alters a material’s optical properties, the optimal conditions for detecting these weak bioelectric signals can be determined. Specifically, In particular, a larger change in reflectivity with respect to incident angle corresponds to higher optical sentivitivity. Motivated by this principle, I began by modeling angle-dependent reflectivity in multilayer devices under s- and p- polarized illumination. To achieve this, I developed a custom Python Transfer Matrix Method (TMM) solver.

### The Setup
* **Target:** Distributed Bragg Reflector (DBR) designed for 561nm.
* **Reference:** Hecht, *Optics* (5th Ed).
* **Materials:** Alternating layers of High Index ($n_H$) and Low Index ($n_L$) dielectrics.

### Results
The graph below shows my simulation output (Blue) compared to the theoretical expectation. The stopband width and reflectivity efficiency match perfectly.

<img src="{{ '/images/561nm.png' | relative_url }}"
     alt="561nm Validation Graph"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

<img src="{{ '/images/Userfriendlyinterface.png' | relative_url }}"
     alt="Userfriendlyinterface"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

<img src="{{ '/images/simulation.png' | relative_url }}"
     alt="Simulation"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

<img src="{{ '/images/comparison.png' | relative_url }}"
     alt="Comparison"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">
### Code Snippet
Here is the core Python function used to generate this matrix:
