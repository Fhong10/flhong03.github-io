---
title: "Reflectivity Modeling of PEDOT:PSS Multilayer Devices Using Transfer Matrix Method"
collection: publications
permalink: /research/project-1/
excerpt: "Validation of a custom Python Transfer Matrix Method solver for electrochromic multilayer reflectivity modeling."
---

Since the current project is ongoing and unpublished, I validated my modeling framework by reproducing results from a previously published study "Dual-Color Optical Recording of Bioelectric Potentials by Polymer Electrochromism". Specifically, I used Fig. 2c from the paper as a benchmark for angle-dependent reflectivity under p-polarized illumination.

## Motivation
Neural recording requires resolving voltage changes as small as 10 µV. By modeling how applied voltage alters a material’s optical properties, the optimal conditions for detecting these weak bioelectric signals can be determined. Specifically, In particular, a larger change in reflectivity with respect to incident angle corresponds to higher optical sentivitivity. Motivated by this principle, I modeled angle-dependent reflectivity in multilayer devices under s- and p- polarized illumination. To achieve this, I developed a custom Python Transfer Matrix Method (TMM) solver.


### Transfer Matrix Method (TMM)

This is a computational framework used to model electromagnetic wave propagation through stratified media.

By enforcing Maxwell’s boundary conditions at each interface, the method relates the electric and magnetic fields of adjacent layers via 2×2 characteristic matrices. The optical response of the entire device—including reflection, transmission, and absorption—is determined by the product of these individual layer matrices. This approach is computationally efficient and essential for optimizing the sensitivity of multilayer thin-film sensors.

### Device Geometry(4-layer devices)
Stack (top → bottom): Laser is entering the bottom layer.

* Aqueous environment-water(semi-infinite layer)
* PEDOT:PSS (≈ 69 nm)
* ITO (≈ 19 nm)
* SF-10 glass prism(semi-infinite layer)
  
<p>Key parameters of the model:</p>
<ul>
  <li>Full complex refractive index handling (n + i·k)
    <ul>
      <li>PEDOT:PSS layer: n = 1.41 + i0.23 <strong>at 561 nm</strong></li>
      <li>PEDOT:PSS layer: n = 1.40 + i0.35 <strong>at 658 nm</strong></li>
    </ul>
  </li>
</ul>
* Incident angle of beam
* Polarization-selective(TE/s-polarization, TM/p-polarization)
* Two wavelengthes comparison(561nm, 658nm)


## Result

<img src="{{ '/images/561nm.png' | relative_url }}"
     alt="561nm Validation Graph"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

The original Fig 2c shows experimental reflectivity data(dotted lines) and theoretical predictions (solid lines). I independently reproduced the theoretical reflectivity curves using my TMM solver and matched them to the published experimental trends at both wavelengths.

<img src="{{ '/images/Userfriendlyinterface.png' | relative_url }}"
     alt="Userfriendlyinterface"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

To facilitate systematic parameter exploration, I implemented a graphical user interface within the Python script using Anaconda. This interface allows users to input material parameters, wavelength, polarization, and incident angle prior to plotting reflectivity curves.

<img src="{{ '/images/simulation.png' | relative_url }}"
     alt="Simulation"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">
     
These are theoretical reflectivity curves generated using my custom Python-based TMM solver.

## Matching

<img src="{{ '/images/comparison.png' | relative_url }}"
     alt="Comparison"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

The simulated reflectivity versus incident angle for p-polarized light at 561 nm and 658 nm shows strong agreement with the published results, confirming the validity of the optical model and parameter implementation.


