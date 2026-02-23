---
layout: default
title: Methods
---

## Experimental & Computational Methods

My work is centered on **methodological rigor**, reproducibility, and the integration of experimental and computational approaches. Below is an overview of the key methods and pipelines I routinely use.

---

## Quantitative Proteomics

### Mass Spectrometry
- LC-MS/MS (DDA and DIA)
- Top-down and bottom-up proteomics
- Crosslinking-MS strategies

**Software**
- MaxQuant
- PEAKS
- DIA-NN

---

## Isotope Labeling Strategies

- SLIM / bSLIM metabolic labeling
- Comparative proteomics across biological conditions
- Statistical validation of protein quantification confidence
### bSLIM labeling strategy

<figure>
  <img src="{{'/assets/img/bSLIM.png' | relative_url }}"
       alt="Schematic overview of the bSLIM metabolic labeling strategy used for quantitative proteomics"
       style="max-width: 600px;"> 
  <figcaption>
    <em>Overview of the bSLIM (bottom-up Simple Light Isotope Metabolic) labeling strategy. The schematic illustrates isotope incorporation, sample mixing, MS acquisition, and quantitative interpretation.</em>
  </figcaption>
</figure>

The bSLIM strategy enables robust quantitative proteomics by leveraging partial isotopic labeling. Unlike complete labeling approaches, bSLIM preserves biological flexibility while allowing accurate estimation of protein abundance changes across conditions.


---

## Computational & Bioinformatics Analysis

### Programming & Data Analysis
- Python (NumPy, SciPy, Pandas, Matplotlib)
- C++ for critical algorithms


**Focus areas**
- Signal processing
- Quantitative confidence assessment
- Algorithm development for proteomics

### Exeample : Molar fraction estimation in bSLIM labeling

To quantify the fraction of non-labelled peptides in bSLIM experiments, I am using a mathematical formulation that relates isotopic incorporation to observed MS signal intensities.

<figure>
  <img src="{{'/assets/img/bSLIM_alpha_fact.png' | relative_url }}"
       alt="Formula used to compute the molar fraction of non-labelled peptides in bSLIM experiments"
       style="max-width: 600px;"> 
  <figcaption>
    <em>Figure — Mathematical formulation used to estimate the molar fraction of non-labelled peptides (α) in bSLIM-based quantitative proteomics.</em>
  </figcaption>
</figure>



---

## Cell Biology & Biochemistry

- Cell culture and protein extraction
- FPLC and biochemical fractionation
- *Xenopus laevis* egg extract preparation
