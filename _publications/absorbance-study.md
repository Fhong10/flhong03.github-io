---
title: "Calculation of Complex Refractive Index"
collection: publications
permalink: /research/project-2/
excerpt: "Extraction of voltage- and wavelength- dependent optcial constants from UV-VIS absorbance for multilayer reflectivity modeling"
mathjax: true
---

## Motivation
Because PEDOT:PSS exhibits voltage- dependent optical absorption, I extracted wavelength- and voltage resolved extinction coefficients rather than assuming a constant k, enabling physically meaningful reflectivity simulations under electrochromical modulation.

### Calcalation
I used UV-Vis spectroscopy to measure absorbance of PEDOT:PSS. The absorbance spectra were obtained experimentally, and the extinction coefficient was then calculated using equations below.

<img src="{{ '/images/Absorbance2.png' | relative_url }}"
     alt="Simulation"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

Voltage- and wavelength- dependent spectra of absorption was measured, as shown in the graph above. These data correspond to the supplementary information in Figure S2a of J. Am. Chem. Soc. 2022, 144, 51, 23505–23515

### Beer-lambert law
$$
A = -\log_{10}\\left(\dfrac{I_{\text{transmitted}}}{I_{\text{incident}}}\right)
$$
A: absorbance
$$
\ln\\left(\frac{I_0}{I}\right) = (\ln 10)\A
$$

### From absorbance to absorption coefficient:
$$
\alpha = \dfrac{ln(10)\A}{d}
$$
where d is film thickness.

Given the absorption coefficient, the extinction coefficient can be calculated.

### Extinction coefficient:
$$
k = \dfrac{\alpha \\lambda}{4\pi}
$$

## Result

The calculated extinction coefficient was 0.233 while real value was 0.20 at 255mV and 561nm, resulting in an error of approximately 10%.

