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
I used UV-Vis spectroscopy to measure absorbance of PEDOT:PSS. Absorbance spectra is measured. Then I used the equations to solve extinction coefficients.

<img src="{{ '/images/Absorbance2.png' | relative_url }}"
     alt="Simulation"
     style="max-width: 420px; width: 100%; height: auto; display: block; margin: 0 0 12px 0;">

Voltage- and wavelength- dependent spectra of absorption is measured like above graph. This is the supplementary data in Figure S2. (a).

### Beer-lambert law
$$
A = -\log_{10}\!\left(\dfrac{I_{\text{transmitted}}}{I_{\text{incident}}}\right)
$$
Where:
* \( A \) is the absorbance (dimensionless).
* \( I_0 \) is the **incident intensity** (light entering the sample).
* \( I \) is the **transmitted intensity** (light passing through).

$$
A = \log_{10}\!\left(\frac{I_0}{I}\right) = \frac{\ln\!\left(\frac{I_0}{I}\right)}{\ln 10} \quad\Rightarrow\quad
\ln\!\left(\frac{I_0}{I}\right) = (\ln 10)\,A
$$

### From absorbance to absorption coefficient:
$$
\alpha = \dfrac{ln(10)\,A}{d}
$$
where d is film thickness.

Since absorption coefficient is given, I can calculate extinction coefficient.

### Extinction coefficient:
$$
k = \dfrac{\alpha \,\lambda}{4\pi}
$$

## Result



