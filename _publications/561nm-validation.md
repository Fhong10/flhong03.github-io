---
title: "Algorithm Validation: 561nm Target"
collection: publications
permalink: /research/project-1/
excerpt: "Benchmarking my Python TMM solver against standard textbook results."
date: 2024-01-01
---

## Project Overview
To verify the accuracy of my Transfer Matrix Method (TMM) simulation code, I reproduced a standard result from optical physics literature.

### The Setup
* **Target:** Distributed Bragg Reflector (DBR) designed for 561nm.
* **Reference:** Hecht, *Optics* (5th Ed).
* **Materials:** Alternating layers of High Index ($n_H$) and Low Index ($n_L$) dielectrics.

### Results
The graph below shows my simulation output (Blue) compared to the theoretical expectation. The stopband width and reflectivity efficiency match perfectly.

![561nm Validation Graph]({{ '/images/561nm.png' | relative_url }})

### Code Snippet
Here is the core Python function used to generate this matrix:
