---
layout: page
title: Treatment Algorithm
subtitle: Diagnosis and control of hypertension in an automated way
header-includes: \usepackage{amsmath}
---

El objetivo de este algoritmo consiste en detectar en que estado de hipertensión se encuentra el paciente tras las correspondientes medidas de la presión sanguínea.

A continuación se muestra un diagrama del algoritmo:

<details open>
<summary><b>Algorithm Diagram</b></summary>
<br>
<img src="/img/algoritme_tractament_Rev3.png" alt="Algorithm Diagram">
</details>

# HTA Intervals Definition

### Normal AT

$$
Normal\,\,\,TA = systolic \leq 129\, \cap \,diastolic\leq 79
$$

In the **Normal AT** stage, the algorithm returns a dialogue with a set of personalized recommendations for the patient based on cardiovascular risk factors.

**Control** in the next 6 Month - 1 year

### Stage I HTA
