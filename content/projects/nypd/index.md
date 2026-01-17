---
title: "An examination of NYPD Stop and Frisk practices using body-worn camera recordings" 
date: 2025-04-21
tags: ["random forest", "entropy balancing", "hierarchical clustering", "doubly robust regression", "policing", "racial disparities", "stop and frisk"]
author: ["Annie Chen"]
description: "Court-commissioned study on constitutional compliance and racial disparities in policing."
cover:
    image: "fmpviz.png"
    alt: "Predicted probabilities of an unconstitutional stop by race"
    relative: true
showToc: false
disableAnchoredHeadings: false

---
The study examined police encounters recorded by body-worn cameras (BWCs) between March 16 and May 15 of 2022. A team of retired New York State judges examined the recordings made by police officers and related documentation of those stopped by police, to determine their compliance with the Fourth Amendment, particularly as enunciated in the seminal Supreme Court case of Terry v. Ohio and the New York Court of Appeals case, People v. De Bour. Participating judges all had years of experience resolving Fourth Amendment search and seizure issues as trial or appellate judges, or both. The concurrence of two judges was required for the identification of an unreported stop or for a finding of constitutionality or unconstitutionality.
 
![](fmpviz.png)

---

#### Statistical Modeling
<div style="display:flex; flex-wrap:wrap; gap:6px;">
  <img alt="Hierarchical Algomerative Clustering" src="https://img.shields.io/badge/Hierarchical%20Clustering-2F81F7?style=for-the-badge">
  <img alt="Random Forest" src="https://img.shields.io/badge/Random%20Forest-2F81F7?style=for-the-badge">
  <img alt="Doubly Robust ML" src="https://img.shields.io/badge/Doubly%20Robust%20ML-2F81F7?style=for-the-badge">
  <img alt="Entity Resolution" src="https://img.shields.io/badge/Entity%20Resolution%20ML-2F81F7?style=for-the-badge">
</div>

#### Software
<div style="display:flex; flex-wrap:wrap; gap:6px;">
  <img alt="Python" src="https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=for-the-badge">
  <img alt="R" src="https://img.shields.io/badge/R-3776AB?logo=r&logoColor=white&style=for-the-badge">
</div>

---

## Highlights

- **Data Engineering & Preprocessing**
    - Processed **1.5M+ BWC recordings** into structured encounters using metadata string matching and **hierarchical clustering** to merge multi-officer recordings of the same incident.
- **Sampling & Study Design**
    - Implemented **stratified random sampling** across encounter types (low-level, stops, arrests/summonses).
    - Conducted post-hoc **power analysis** and calculated **minimum detectable effect sizes (MDES)** to gauge statistical precision in subgroup and disparity analyses.
- **Feature Engineering from Unstructured Video**
    - Research assistants trained to apply systematic **content coding protocols** to extract event-level variables (officer actions, civilian engagement, encounter type).
    - Entity resolution of encounters by linking structured video metadata to administrative reports.
- **Ground-Truth Labeling & Reliability**
    - Retired judges coded stop constitutionality under **Fourth Amendment standards**.
    - Used **Cohen’s κ** to measure inter-rater reliability; applied majority-rule consensus for labels.
- **Statistical Modeling & Inference**
    - Fit **logistic regression models** to predict unconstitutional stops based on encounter conditions (e.g., self-initiated vs. call-driven, Neighborhood Safety Team presence).
    - Applied a **doubly robust estimation framework** using **entropy balancing** to adjust for covariate imbalance and strengthen inference.
    - Estimated uncertainty with **robust standard errors** and **95% confidence intervals**.


---

## Click here for the [full report.](https://www.nypdmonitor.org/wp-content/uploads/2025/05/2025.05.01-956-ISLG-Report-An-Examination-of-NYPD-Stop-and-Frisk-Practices.pdf)

---


## Citation

Chen, Annie Y., and Kathleen Doherty. 2025. An Examination of NYPD Stop and Frisk Practices: Using Body-Worn Camera Recordings to Determine the Constitutionality and Documentation of Street Stops. CUNY Institute for State and Local Governance. Research. https://www.nypdmonitor.org/wp-content/uploads/2025/05/2025.05.01-956-ISLG-Report-An-Examination-of-NYPD-Stop-and-Frisk-Practices.pdf.

```BibTeX
@article{
    fmp2025,
	author = {Chen, Annie Y. and Doherty, Kathleen},
    month = Apr,
	year = {2025},
	title = {An {Examination} of {NYPD} {Stop} and {Frisk} {Practices}: {Using} {Body}-worn {Camera} {Recordings} to {Determine} the {Constitutionality} and {Documentation} of {Street} {Stops}},
	institution = {CUNY Institute for State and Local Governance},
    publisher = {NYPD Monitor},
    url = {Denerstein - encounters that officers categorized as a low-leve.pdf:files/8403/Denerstein - encounters that officers categorized as a low-leve.pdf:application/pdf}}
```
