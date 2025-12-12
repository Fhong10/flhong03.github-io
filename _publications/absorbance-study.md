---
title: "Calculation of Complex Refractive Index"
collection: publications
permalink: /research/project-2/
excerpt: "Detailed study of material absorbance properties across the visible spectrum."
mathjax: true
---

## Motivation
To model reflectivity in multilayer device, refractive index is the important parameter. Especially, refractive index comprises of real part and imaginary part (n+ik). I calculated imaginary part which is extinction coefficient.

### Calcalation
I used UV-Vis spectroscopy to measure absorbance of PEDOT:PSS. Then I used the equations to solve extinction coefficients.

$$
A = -\log_{10}\!\left(\dfrac{I_{\text{transmitted}}}{I_{\text{incident}}}\right)
$$
where \( I_{\text{incident}} \) is the intensity of light entering the PEDOT:PSS sample and \( I_{\text{transmitted}} \) is the intensity after passing through the sample. Absorbance is a **dimensionless** quantity. It is the base‑10 logarithm of the transmitted-to-incident intensity ratio.

From absorbance to absorption coefficient \( \alpha \):
$$
\alpha = \dfrac{2.303\,A}{d}
$$
where \( d \) is film thickness.

Extinction coefficient \( k \):
$$
k = \dfrac{\alpha \,\lambda}{4\pi}
$$

## Conclusion
The material shows strong absorption in the UV-Blue region, tapering off towards the Red/IR, which is consistent with the bandgap energy of...

<img src="{{ '/images/Absorbance2.png' | relative_url }}"
     alt="Simulation"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

