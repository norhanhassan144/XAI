# **Random Forest Model Explanation using PDP, SHAP, and LIME**

## **Project Overview**
This project demonstrates how to explain a Random Forest model's predictions using three popular interpretability techniques:
1. **Partial Dependence Plot (PDP)**
2. **SHAP (SHapley Additive exPlanations)**
3. **LIME (Local Interpretable Model-agnostic Explanations)**

The dataset used is the **Adult Income Dataset** from the UCI Machine Learning Repository, which aims to predict whether an individual earns more than 50K or not based on various features such as age, education, and hours worked per week.

---

## **Technologies Used**
- Python
- Pandas
- NumPy
- scikit-learn
- Matplotlib
- LIME
- SHAP

---
## Project Results

### 1. Partial Dependence Plot (PDP):
- **Age**: As age increases from 20 to 50 years, the likelihood of earning more than 50K increases.
- **Marital Status**: Being married increases the chances of earning more than 50K.
- **Hours per Week**: People working more than 40-50 hours per week are more likely to earn more than 50K.

### 2. SHAP:
- **Summary Plot**: Visualizes the contribution of each feature, showing that `capital-gain` and `education-num` are significant for predictions.
- **Interaction Plot**: Demonstrates how features like `age` interact with other features, with most interactions being weak.

### 3. LIME:
- **Local Explanation**: For an individual prediction, LIME shows that:
  - The person has no capital gain (`capital-gain ≤ 0`), contributing 58% to the prediction.
  - The person has education above 12 years (`education-num > 12`), contributing 13%.
  - The person works more than 45 hours per week (`hours-per-week > 45`), contributing 9%.
