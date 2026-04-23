# Exploratory Data Analysis (EDA) Summary

## 1. Data Cleaning & Preparation

* Standardized column names and categorical values for consistency
* Missing values (`?`) were replaced with "unknown" to preserve dataset size
* Target variable `income` was converted into binary format (0 = ≤50K, 1 = >50K)
* Irrelevant feature `fnlwgt` was removed as it represents sampling weight
* Duplicate records were dropped

---

## 2. Distribution Analysis

### Numerical Features

* **Age** shows a moderately right-skewed distribution, concentrated between 25–50
* **Hours per week** is tightly centered around 40, indicating standard work patterns
* **Capital gain and capital loss** are highly skewed with the majority of observations at 0 and a few extreme values

---

## 3. Outlier Analysis

* Outliers are present across all numerical features, especially in capital-related variables
* These extreme values were retained as they reflect valid real-world observations rather than data errors

---

## 4. Numerical Relationship with Income (Pearson Correlation)

* All numerical variables show **positive but weak correlation** with income
* **education_num (~0.33)** has the strongest correlation among numerical features
* Other variables:

  * capital_gain (~0.23)
  * hours_per_week (~0.22)
  * age (~0.21)
  * capital_loss (~0.15)
* All relationships are statistically significant (p < 0.05)

Indicates that numerical features alone are not strong drivers of income

---

## 5. Categorical Relationship with Income (Chi-Square & Cramér’s V)

All categorical variables are statistically significant (p < 0.05)

### Strength of Association:

* **Strong:**

  * relationship (~0.45)
  * marital_status (~0.44)

* **Moderate:**

  * education (~0.36)
  * occupation (~0.33)

* **Low to Moderate:**

  * sex (~0.21)
  * workclass (~0.18)

* **Weak:**

  * race (~0.11)
  * native_country (~0.10)

Categorical features show stronger association with income compared to numerical features

---

## 6. Key Patterns Observed

* Individuals categorized as **Husband** have the highest proportion of >50K income
* **Married individuals** show significantly higher probability of earning >50K compared to never-married
* Higher levels of **education** correspond to increased likelihood of higher income
* **High-skill occupations** (e.g., exec_managerial, prof_specialty) have higher income proportions

---

## 7. Anomalies & Exceptions

* Some individuals with higher education still fall in ≤50K category
* Certain high-skill occupations include individuals earning ≤50K
* Instances of high capital gain are also observed in ≤50K group


These exceptions indicate that income is influenced by multiple interacting factors rather than a single variable

---

## 8. Conclusion

The analysis shows that **categorical variables**, particularly relationship status, marital status, education, and occupation, have stronger associations with income compared to numerical features.

The presence of weak numerical correlations and multiple anomalies suggests that income prediction requires considering combined effects of multiple variables rather than relying on any single feature.

---
