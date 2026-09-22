# Healthcare-EDA
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-darkblue.svg?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-📊-orange.svg?style=for-the-badge)](https://seaborn.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

An advanced, end-to-end Exploratory Data Analysis (EDA) portfolio project identifying critical clinical and demographic risk factors associated with patient strokes[cite: 1]. This project uncovers hidden pathways to stroke events using robust statistical profiling, feature distributions, and multivariate analysis[cite: 1].

---

## 🎯 Project Overview & Problem Statement

Strokes are dangerous, sudden, and life-threatening medical anomalies[cite: 1]. However, many foundational clinical markers—such as blood pressure anomalies, chronic high blood sugar, elevated body mass indexes, and lifestyle history—can be systematically managed if high-risk profiles are flagged early enough[cite: 1].

### The Objective
To perform detailed exploratory data profiling on clinical datasets to extract high-impact, actionable insights[cite: 1]. By translating raw features into precise patient risk streams, this project demonstrates how statistical anomalies and multivariate relationships can serve as pre-clinical alert systems[cite: 1].

---

## 🔬 Core Research Hypotheses

The analytical architecture of this project was constructed around testing three core research assumptions:

1. **Hypothesis 1:** Older patients with pre-existing clinical complications like hypertension (high blood pressure) and hyperglycemia (elevated blood glucose) present an exponentially higher statistical risk of stroke[cite: 1].
2. **Hypothesis 2:** Patients with a history of tobacco exposure (`formerly smoked` or `smokes`) display a higher relative rate of stroke incidence compared to the control group who `never smoked`[cite: 1].
3. **Hypothesis 3:** Individuals falling into extreme Body Mass Index (BMI) ranges are strongly associated with higher stroke likelihood due to underlying metabolic strain[cite: 1].

---

## 🗂️ Dataset Architecture & Column Profiling

The model consumes a healthcare tracking repository containing unique clinical variables mapped per patient[cite: 1]:

| Feature Name | Type | Description | Easy Breakdown |
| :--- | :--- | :--- | :--- |
| `id` | Categorical | Unique Identifier | Individual Patient tracking token[cite: 1]. |
| `age` | Numerical | Patient Age | Evaluated continuously from infancy through 80+[cite: 1]. |
| `hypertension` | Binary | High Blood Pressure | `0` = Normal Baseline, `1` = Diagnosed Hypertension[cite: 1]. |
| `heart_disease` | Binary | Cardiovascular Health | `0` = No recorded disease, `1` = Diagnosed Heart Condition[cite: 1]. |
| `ever_married` | Binary | Relationship History | Marital status category (`Yes` / `No`)[cite: 1]. |
| `work_type` | Categorical | Employment Sector | Occupational category (e.g., `Self-employed`, `Private`)[cite: 1]. |
| `Residence_type` | Categorical | Environmental Setting | Geolocation tracking category (`Urban` vs `Rural`)[cite: 1]. |
| `avg_glucose_level` | Numerical | Blood Sugar Metric | Continuous blood glucose levels measured via blood work[cite: 1]. |
| `bmi` | Numerical | Body Mass Index | Patient weight-to-height ratio metric[cite: 1]. |
| `smoking_status` | Categorical | Tobacco History | Four-tier split: `never smoked`, `formerly smoked`, `smokes`, `Unknown`[cite: 1]. |
| **`stroke`** | Binary | **Target Variable** | **`0` = No Stroke Event Recorded, `1` = Stroke Occurred.**[cite: 1] |

---
<img width="1664" height="928" alt="1780731409" src="https://github.com/user-attachments/assets/ae94554a-cd2f-43ae-b1cc-d6df16121cf0" />


## 📊 WHAT I FOUND FROM EDA (Key Discoveries)

### 1. Data Integrity & Robust Outlier-Safe Imputation
* **The Challenge:** Initial profiling flagged missing values in the `bmi` feature column[cite: 1]. The BMI field contained extreme right-skewed values peaking as high as `97.6`[cite: 1]. Using a simple mean average would artificially pull values upward[cite: 1].
* **The Solution:** Imputed missing indices using the column **Median (`28.1`)**[cite: 1]. The median acts as an outlier-safe statistical anchor, preserving the true distributional core of the column[cite: 1].

### 2. Age is the Undisputed Dominant Driver
* **The Top Predictor:** In matrix correlation modeling, `age` and `Age_Group_Senior` hold the strongest direct positive correlation with stroke events[cite: 1]. Getting older is the single dominant driver in this dataset[cite: 1].
* **The Youth Baseline:** Young populations and children show minimal to near-zero stroke incidence, bypassing the risk pipelines entirely[cite: 1].

### 3. Blood Glucose Levels Reveal a High-Risk "Stretch"
* **Healthy Baseline:** For the non-stroke control group, glucose levels are heavily concentrated below `115 mg/dL`, representing a stable, healthy baseline[cite: 1].
* **The Stroke Window:** The top 50% of stroke patients exhibit significantly elevated, volatile glucose levels stretching from `105 mg/dL` all the way up to `200+ mg/dL`[cite: 1].

### 4. The BMI Statistical Floor
* **Narrow Risk Concentration:** While the non-stroke group displays massive variance (spreading from 10 to 98 BMI), the stroke group is highly restricted[cite: 1]. 
* **The Floor:** The lower whisker of the stroke group stops abruptly around a BMI of `20`[cite: 1]. This indicates a potential statistical floor—strokes are almost non-existent in underweight individuals within this dataset[cite: 1].

### 5. The Clinical Risk Layer
* **Hypertension & Heart Disease:** Stroke percentages are heavily elevated among hypertensive patients and heart disease patients, confirming that cardiovascular health strongly impacts stroke risk[cite: 1]. They form a tight secondary medical risk layer tied in correlation strength[cite: 1].


## 🏁 Conclusion

This Exploratory Data Analysis successfully validates that stroke occurrence is rarely sparked by a single, isolated feature[cite: 1]. Instead, it is catalyzed by a combination of factors[cite: 1]. Advanced age acts as the primary gatekeeper, but when paired with an elevated blood glucose stretch (105–200+ mg/dL), active/historical tobacco use, and a restrictive BMI window (27–32), the risk path amplifies dramatically[cite: 1]. Early pre-clinical monitoring must focus on these intersecting multivariate profiles to effectively intercept stroke events before they occur[cite: 1].

---

## 👤 Author

**Shraddha Bisht**  
*Data Scientist*
