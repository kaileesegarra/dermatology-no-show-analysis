# Predicting Medical Appointment No-Shows with Logistic Regression

**Author:** Kailee Segarra  
**Course:** CMPS 6790 – Data Science  

🔗 **Live Project:**  
https://kaileesegarra.github.io/dermatology-no-show-analysis/

---

## Overview

Missed medical appointments (no-shows) are a significant operational challenge in healthcare systems. They lead to unused appointment slots, increased wait times, delayed care, and inefficiencies for both providers and patients.

This project uses **data science and machine learning** to explore whether patient, scheduling, and reminder-related variables can be used to **predict appointment no-shows**.

The goal is not just prediction, but **actionable insight**—helping clinics better understand patient behavior and improve scheduling strategies.

---

## Key Question

> **Can scheduling, demographic, and behavioral variables predict whether a patient will miss a medical appointment?**

---

## Dataset

- **Source:** [Kaggle – Brazilian Medical Appointment No-Show Dataset](https://www.kaggle.com/datasets/joniarroba/noshowappointments)  
- **Size:** 100,000+ appointment records  
- **Features include:**
  - Age
  - Gender
  - Appointment scheduling date
  - SMS reminders
  - Health conditions (e.g., diabetes, hypertension)
  - Neighborhood information
  - Appointment outcome (attended vs. no-show)

---

## Approach

This project follows a full data science workflow:

1. **Data Cleaning & Feature Engineering**
   - Created `lead_time_days` (days between scheduling and appointment)
   - Converted categorical variables
   - Standardized numerical features

2. **Exploratory Data Analysis (EDA)**
   - Identified key predictors:
     - Scheduling delay
     - Age
     - SMS reminder patterns
     - Appointment weekday
   - Explored interaction effects (e.g., age × delay)

3. **Modeling**
   - Built a **logistic regression classifier**
   - Used a **train/test split** for evaluation

4. **Evaluation**
   - Accuracy
   - Precision
   - Recall (primary focus)
   - F1 Score
   - ROC-AUC

---

## Key Findings

- **Scheduling delay is the strongest predictor**
  - Longer lead times → higher no-show rates

- **Age influences attendance patterns**
  - Different age groups exhibit different behaviors

- **SMS reminders require careful interpretation**
  - Higher no-show rates among SMS recipients likely reflect **targeting high-risk patients**, not ineffectiveness

- **Interaction effects matter**
  - Combining scheduling delay + age provides deeper insight than either alone

---

## Model Insights

- Logistic regression provides a **strong, interpretable baseline**
- Model achieves **moderate performance** with balanced trade-offs
- **Recall is prioritized**, allowing identification of high-risk no-show patients

---

## Real-World Applications

This model can support:

- Targeted reminder strategies for high-risk patients  
- Improved scheduling policies (e.g., reducing long lead times)  
- Proactive outreach and patient engagement  
- Data-driven clinic operations  

---

## Limitations

- Observational data (no causal conclusions)
- Dataset from Brazilian healthcare system (limited generalizability)
- Missing features such as:
  - Distance to clinic
  - Appointment type
  - Prior attendance history

---

## Future Improvements

- Test more advanced models (Random Forest, Gradient Boosting)
- Incorporate additional features (geographic + behavioral)
- Optimize threshold for real-world deployment
- Build a dashboard for clinical use

---

## Tech Stack

- Python  
- Pandas  
- NumPy  
- Matplotlib / Seaborn  
- Scikit-learn  
- Google Colab  

---

## Key Takeaway

Even simple, interpretable models like logistic regression can uncover meaningful patterns in patient behavior and provide actionable insights for improving healthcare operations.

---
