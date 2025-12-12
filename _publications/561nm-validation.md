---
title: "Reflectivity Modeling of PEDOT:PSS Multilayer Devices Using Transfer Matrix Method"
collection: publications
permalink: /research/project-1/
excerpt: "Benchmarking my Python TMM solver against standard textbook results."
date: 2024-01-01
---

## Motivation
Neural recording requires resolving voltage changes as small as 10 µV. By modeling how applied voltage alters a material’s optical properties, the optimal conditions for detecting these weak bioelectric signals can be determined. Specifically, In particular, a larger change in reflectivity with respect to incident angle corresponds to higher optical sentivitivity. Motivated by this principle, I began by modeling angle-dependent reflectivity in multilayer devices under s- and p- polarized illumination. To achieve this, I developed a custom Python Transfer Matrix Method (TMM) solver.

### Device Geometry(4-layer devices)
Stack (top → bottom):
* SF-10 glass prism(semi-infinite layer)
* ITO (≈ 19 nm)
* PEDOT:PSS (≈ 69 nm)
* Aqueous environment-water(semi-infinite layer)

Key parameters of the model:
* Full complex refractive index handling (n+ik)
* Incident angle of beam
* Polarization-selective(TE/s-polarization, TM/p-polarization)
* Two wavelengthes comparison(561nm, 658nm)

## Result

Since what I have done is not published yet, I modeled reflectivity on previous published paper "Dual-Color Optical Recording of Bioelectric Potentials by Polymer Electrochromism". I used Fig.2(c) to match simulation and Fig.2C.

<img src="{{ '/images/561nm.png' | relative_url }}"
     alt="561nm Validation Graph"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

This is original Fig 2c in the paper. Dotted lines are experimental data and lines are theoretical graphs done by the author. I am going to match my simulation graph to lines in the diagram.

<img src="{{ '/images/Userfriendlyinterface.png' | relative_url }}"
     alt="Userfriendlyinterface"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

I made the script and used anaconda to run Python script. Before plotting the graph, I made this user interface to enter the parameters to plot the graphs.

<img src="{{ '/images/simulation.png' | relative_url }}"
     alt="Simulation"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

This is my theoretical graphs. Reflectivity versus incident angle using p-polarized light. Since there are two wavelenghts, there are two graphs generated.

<img src="{{ '/images/comparison.png' | relative_url }}"
     alt="Comparison"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

I matched two theoretical reflectivity graphs to experiemntal data(dotted lines) in the diagram. Those two align with each other well.


