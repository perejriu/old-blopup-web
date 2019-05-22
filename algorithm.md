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
$$ $$
$$
\[ \begin{cases}
      0 & x\leq 0 \\
      \frac{100-x}{100} & 0\leq x\leq 100 \\
      0 & 100\leq x
   \end{cases}
\]
$$
