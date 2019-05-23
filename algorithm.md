---
layout: page
title: Treatment Algorithm
subtitle: Diagnosis and control of hypertension in an automated way
header-includes: \usepackage{amsmath}
---

The goal of this algorithm is to detect in which state of hypertension the patient belongs after the corresponding measurements of blood pressure.

Here, there is a flux-diagram of the algorithm:

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


## Normal AT
>
$$
Normal\,\,\,TA = systolic \leq 129\, \cap \,diastolic\leq 79
$$

In the **Normal AT**:

* The **Control** should be in the next **6 Month - 1 year**.

* The algorithm returns a dialogue with a set of personalized recommendations for the patient based on cardiovascular risk factors.


<p style='text-indent: 1em'>esto es una prueba de style='text-indent: 1em'</p>

<details close>
<summary><b>Here there is an example of the dialogue:</b></summary>
<br>
<img src="/img/algoritme_tractament_Rev3.png" alt="Treatment dialogue">
</details>

## Stage I HTA
>
$$
Stage\,\,\,I\,\,\,HTA = systolic \in [130, 139]\, \cup  \,diastolic\in [80, 89]\
$$

In **Stage I HTA**:
  * The algorithm returns the **personalized recommendations** like before.  

  * Notifies the doctor, and afterwards he decide to give or not to give **pharmacotherapy**.  

  * The **Control** should be in the next **3 months - 6 months**.  

## Stage II hostname

>
$$
Stage\,\,\,II\,\,\,HTA = systolic \geq 140\, \cup \,diastolic\geq 90
$$

In **Stage I HTA** there are _sub-stages_

### Stage II A
>
$$
Stage\,\,\,II\,\,\,A = systolic \in [140, 149]\, \cup  \,diastolic\in [90, 99]\
$$

#### Asymptomatic
  * The algorithm returns the **personalized recommendations** like before.  

  * The **Control** should be in the next **15 days - 1 month**.  

#### Symptomatic

> Symptomatic means that the patient feels **headaches** and / or **dizziness**

* Notification to the doctor to decide if the patient should take **pharmacotherapy**

* The algorithm returns the **personalized recommendations** like before.

* The **Control** should be in the next **15 days - 1 month**.  


### Stage II B
>
$$
Stage\,\,\,II\,\,\,B = systolic \in [160, 179]\, \cup  \,diastolic\in [100, 109]\
$$

* **Non-pharmacological treatment**. The algorithm returns personalized recommendations based on risk factors of the patient.

* **Pharmacotherapy**. Show the _Medication Suggestion Screen_  
  * _The Medication Suggestion Screen still needs to be designed and implemented_

* **Notify** the doctor in order to know the situation of the patient.

* The **Control** should be in the next **15 days**.  

### Stage II C
>
$$
Stage\,\,\,II\,\,\,C = systolic \geq 180\, \cup \,diastolic\geq 110
$$

The patient needs **inmediate medical care**. The app shows a message telling the handworker to go to the hospital.
