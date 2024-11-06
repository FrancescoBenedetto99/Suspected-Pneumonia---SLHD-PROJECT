# Suspected Pneumonia Mortality Prediction Model

Project for the Statistical Learning for Healthcare Data course held at Politecnico di Milano by Professor Manuela Ferrario.

## Project Overview

The goal of this project is to develop a predictive model that estimates the mortality of critically ill patients suspected of having pneumonia. The dataset used includes data from 585 patients with varying types of pneumonia, such as COVID-19, bacterial pneumonia, and other viral types. The key objective is to predict patient mortality by analyzing clinical features and understanding the factors contributing to patient outcomes. Special attention is given to clinical parameters such as bronchoalveolar lavage (BAL) and ICU length of stay.

---

## Database Description

The **Suspected Pneumonia** dataset, provided by PhysioNet, contains data for 585 patients suspected of having pneumonia. These patients were critically ill, received mechanical ventilation, and often underwent bronchoalveolar lavage (BAL) as part of their treatment. The dataset includes detailed information, including 12,495 patient-ICU-days and 44 clinical parameters, such as vital signs, laboratory tests, and mechanical support devices.

### Key Details:
- **Patients**: 585 (190 with COVID-19, 50 with pneumonia secondary to other respiratory viruses, 252 with bacterial pneumonia, and 93 non-pneumonia controls)
- **Outcomes**: 45% of the cohort had an unfavorable outcome (death or hospice discharge)
- **Episodes**: 136 community-acquired pneumonia (CAP), 214 hospital-acquired pneumonia (HAP), and 328 ventilator-associated pneumonia (VAP)
- **Data**: Includes granular per-day information, along with expert clinician adjudications.

For further details, you can explore the following resource:
- [PhysioNet Suspected Pneumonia Dataset Paper](https://physionet.org/content/script-carpediem-dataset/1.1.0/)
  
---

## Overall Objectives

The primary goal of this project is to predict mortality using ICU data. 


1. **Model Development**: Build a model to predict patient mortality based on ICU data, such as demographics, clinical parameters, and pneumonia episode details.
2. **Key Parameters**: Identify significant features for the model, with a focus on clinical data, demographics, and pneumonia characteristics.
3. **Integration of BAL Data**: Investigate how to incorporate the `has_bal` feature (indicating whether a patient underwent bronchoalveolar lavage) into the prediction model.

---

## Model Objective

The model should account for:

- **Patient Demographics**: Age, gender, ethnicity, etc.
- **Clinical Parameters**: SOFA score, vital signs, mechanical support devices, etc.
- **Pneumonia-related Data**: Pneumonia type, BAL information, and episode outcomes.

The model will predict mortality on a day-by-day basis during ICU stays, while also handling missing or inconsistent data. Special attention will be paid to the incorporation of the `has_bal` feature, which indicates whether the patient underwent bronchoalveolar lavage.

**Key Considerations**:
- Handling **ICU length of stay variations**: The model should account for patients who stay longer in the ICU and incorporate day-by-day data for each patient.
- Defining **Inclusion/Exclusion Criteria**: The dataset should carefully filter patients based on criteria like age, pneumonia type, and clinical status to ensure a representative sample.

### Optional Enhancements
An optional enhancement for this project involves building a system that allows the model to automatically update as new patient data is collected. This will help the model remain accurate over time as new data emerges.

---

## Online Learning Simulation

The online learning simulation focuses on adapting the predictive model over time. It uses the **CarpeDiem dataset** to predict the mortality of patients suffering from pneumonia. In this simulation, ICU data for each patient is arranged chronologically, with specific dates assigned to each ICU day.

### Key Features of the Simulation:

1. **Initial Model Training**:
   - The model is first trained on data from the first month of ICU stays to establish a solid baseline.
   
2. **Online Learning Process**:
   - Following the initial training, the model is updated weekly as new data becomes available. This process simulates a real-world scenario where data is continuously collected, and the model is periodically updated to reflect new trends or patterns.
   
3. **Periodic Updates**:
   - The model undergoes continuous refinement as new patient data is introduced, allowing it to adapt to emerging trends in mortality prediction.

### Goal of Online Learning:

- **Adaptation to New Data**: The objective of this simulation is to ensure that the model can maintain its predictive power over time by continuously learning from fresh data, keeping it relevant in dynamic healthcare settings.
- **Real-World Applicability**: This online learning approach simulates the ongoing need for models to evolve in response to ever-changing patient data, ensuring they remain accurate and reliable for clinicians.

---

## Conclusion

This project demonstrates how machine learning can be applied to real-world medical datasets to predict patient mortality, specifically in the context of pneumonia. By incorporating patient demographics, clinical data, and pneumonia-related features, the model can support clinicians in making informed decisions about patient care in the ICU.

Moreover, the integration of online learning highlights how predictive models can stay current by updating regularly with new data, ensuring that healthcare providers have access to the most accurate predictions as they evolve over time.

---

## Authors

- Francesco Benedetto
- Carlotta Pagani
- Riccardo Sena

---
