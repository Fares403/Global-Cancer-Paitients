# Global Cancer Patients Classification

## Overview

This project focuses on classifying cancer severity levels (**Mild**, **Moderate**, **Severe**) using a machine learning pipeline. The pipeline integrates **feature selection** via Random Forest, **dimensionality reduction** with Linear Discriminant Analysis (LDA), and final classification using a **Support Vector Classifier (SVC)**.

The dataset includes records of cancer patients across various countries from 2015 to 2024, with demographic, lifestyle, and medical features.

---

## Project Objectives

* Transform continuous severity scores into categorized severity levels.
* Select informative features using a Random Forest model.
* Reduce dimensionality with LDA for improved separation and model performance.
* Train an SVC model to classify patients based on the processed features.
* Achieve high accuracy and interpretability.

---

## Dataset Description

The dataset includes the following:

* **Demographics**:

  * `Patient_ID`, `Country`, `Region`, `Year`
  * `Age`, `Gender`

* **Lifestyle & Environmental Factors**:

  * `Genetic_Risk`, `Air_Pollution`, `Alcohol_Use`, `Smoking`, `Obesity_Level`

* **Medical Information**:

  * `Cancer_Type`, `Cancer_Stage`
  * `Treatment_Cost`, `Survival_Years`

* **Target**:

  * Original numerical score (continuous)
  * Converted to 3 classes:

    * `Mild`: Target < 4
    * `Moderate`: 4 ≤ Target < 6
    * `Severe`: Target ≥ 6

---

## Methodology

### 1. Preprocessing

* Handled categorical variables using Label Encoding and One-Hot Encoding.
* Split dataset into training and testing sets (80/20).

### 2. Feature Selection

* Applied **Random Forest** to evaluate feature importance.
* Selected the most significant features for classification.

### 3. Dimensionality Reduction

* Applied **Linear Discriminant Analysis (LDA)** to project data into a lower-dimensional space while maximizing class separability.

### 4. Classification

* Trained a **Support Vector Classifier (SVC)** on the transformed features.
* Evaluated model using accuracy, confusion matrix, and classification report.

---

## Results

* **Final Accuracy**: **97%**
* The combined approach of feature selection + LDA + SVC significantly improved classification performance.
* The model shows strong potential for assisting in preliminary cancer severity assessment.

---

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/Fares403/Global-Cancer-Paitients.git
   cd Global-Cancer-Paitients
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Open and run the notebook:

   ```bash
   jupyter notebook Notebook.ipynb
   ```

---

## Future Enhancements

* Apply GridSearchCV for hyperparameter tuning.
* Explore ensemble methods like XGBoost or Stacking.
* Add SHAP analysis for feature contribution visualization.
* Deploy the model with a basic frontend using Streamlit or Flask.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

Would you like me to format this as a downloadable `README.md` file for you?
