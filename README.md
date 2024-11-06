# Suspected Pneumonia Mortality Prediction Model

Project for the Statistical Learning for Healthcare Data course held at @Politecnico di Milano.

## Project Overview

This project aims to develop a predictive model for estimating the mortality risk of critically ill patients suspected of having pneumonia. The dataset used includes data from 585 patients with various types of pneumonia (e.g., COVID-19, bacterial, viral). The model analyzes clinical features to predict patient mortality, with a focus on clinical parameters such as bronchoalveolar lavage (BAL) and ICU length of stay.

---

## Database Description

The **Suspected Pneumonia** dataset, provided by PhysioNet, contains data for 585 critically ill patients suspected of having pneumonia. These patients received mechanical ventilation and often underwent bronchoalveolar lavage (BAL) as part of their treatment. The dataset includes 12,495 patient-ICU-days and 44 clinical parameters.

### Key Details:
- **Patients**: 585 (190 with COVID-19, 50 with pneumonia from other respiratory viruses, 252 with bacterial pneumonia, and 93 non-pneumonia controls)
- **Outcomes**: 45% had an unfavorable outcome (death or hospice discharge)
- **Episodes**: 136 community-acquired pneumonia (CAP), 214 hospital-acquired pneumonia (HAP), and 328 ventilator-associated pneumonia (VAP)
- **Data**: Includes granular per-day information, with expert clinician adjudications.

For more details, visit the [PhysioNet Suspected Pneumonia Dataset Paper](https://physionet.org/content/script-carpediem-dataset/1.1.0/).

---

## Model Objective

The model aims to predict patient mortality on a day-by-day basis using clinical features, demographics, and pneumonia-related data.

Key considerations:
- **Patient Demographics**: Age, gender, ethnicity, etc.
- **Clinical Parameters**: SOFA score, vital signs, mechanical support devices, etc.
- **Pneumonia-related Data**: Pneumonia type, BAL status, and episode outcomes.
- **ICU Stay Variability**: The model accounts for variations in ICU length of stay and incorporates day-by-day data for each patient.

**Key Focus**: Incorporating the `has_bal` feature (whether the patient underwent bronchoalveolar lavage) into the prediction model.

---

## Online Learning Simulation

This simulation focuses on updating the model over time as new ICU data becomes available, simulating a real-world scenario where the model adapts to emerging trends.

### Key Features:
1. **Initial Model Training**: The model is trained on the first month of ICU data.
2. **Online Learning Process**: The model is updated weekly with new patient data.
3. **Periodic Updates**: Continuous refinement of the model to adapt to new mortality trends.

The goal is to maintain the model's predictive accuracy as it learns from new data, ensuring its relevance in a dynamic healthcare environment.

---

## Conclusion

This project demonstrates how machine learning can predict patient mortality, specifically in the context of pneumonia. By integrating clinical data and patient demographics, the model can assist healthcare professionals in making more informed decisions in the ICU. Additionally, the online learning approach ensures that the model stays current with new data.

---
