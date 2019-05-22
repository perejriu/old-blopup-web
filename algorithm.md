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


There are three essential intervals given the BP values:
* <span style="color:green">Normal AT</span>.
* <span style="color:yellow">Stage I HTA</span>.
* <span style="color:red">Stage II HTA</span>.
>
Every interval is related with a face:


### Normal AT
>
$$
Normal\,\,\,TA = systolic \leq 129\, \cap \,diastolic\leq 79
$$

In the **Normal AT**:
* The algorithm returns a dialogue with a set of personalized recommendations for the patient based on cardiovascular risk factors.

<details close>
<summary><b>Here there is an example of the dialogue:</b></summary>
<br>
<img src="/img/algoritme_tractament_Rev3.png" alt="Treatment dialogue">
</details>

* The **Control** should be in the next 6 Month - 1 year.

### Stage I HTA
>
$$
Normal\,\,\,TA = systolic \in [130, 139]\, \cup  \,diastolic\in [80, 89]\
$$

In **Stage I HTA**:
  * The algorithm returns the **personalized recommendations** like before.
  * Notifies the doctor, and afterwards he decide to give or not to give **pharmacotherapy**.
  * The **Control** should be in the next 6 Month - 1 year.
