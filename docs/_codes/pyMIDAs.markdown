---
layout: post
title: "pyMIDAs "
date:   2020-07-28 20:22:13 +0200
abstract: "pyMIDAs"
featured_img: /assets/img/GitHub-Mark-32px.png
number: 4
---

# pyMIDAs

<a href="https://github.com/Nohic56/pyMIDAs" style="color: dodgerblue;">pyMIDAs</a>

## MIDAs (Molecular Isotopic Distribution Analysis)

MIDAs is a software designed to compute the theoretical isotopic distribution for molecules of known elemental composition. MIDAs computes for a molecule simultaneously two isotopic distributions: the coarse-grained isotopic distribution and the fine-grained isotopic distribution.

Web interface: [MIDAs](https://www.ncbi.nlm.nih.gov/CBBresearch/Yu/midas/index.html) and the 
C++ source code: [FTP](https://ftp.ncbi.nlm.nih.gov/pub/qmbp/qmbp_ms/MIDAs)

Original publication from Gelio Alves and Yi-Kuo Yu at [QMBP](https://www.ncbi.nlm.nih.gov/CBBresearch/Yu/index.html)

- *Alves, Gelio et al.* **“Molecular Isotopic Distribution Analysis (MIDAs) with adjustable mass accuracy.”** Journal of the American Society for Mass Spectrometry vol. 25,1 (2014): 57-70. [![DOI:10.1007/s13361-013-0733-7](https://zenodo.org/badge/DOI/10.1007/978-3-319-76207-4_15.svg)](https://doi.org/10.1007/s13361-013-0733-7)


Additionally, a scoring function has been developed and added to this package by Nicolas Senecaut and Jean-Michel camadro.
### License

MiDAS is released under the MIT License. See the LICENSE file for details.
Authors

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)


### Features
#### General
- Easy-to-use Python interface for integrating MIDAs into existing workflows.
- Extensible architecture allowing for customization and integration with other tools.
#### isotopic distribution
- Compute fine-grained isotopomer distributions for metabolites based on their chemical formula and experimental conditions.
- Support for different methods of isotopic distribution analysis, including polynomial-based and FFT-based methods.
#### Scoring distribution
- function computes the root mean square error (RSE) between two sets of data points: experimental and theoretical probabilities. It measures the deviation between the observed experimental probabilities and the expected theoretical probabilities.
