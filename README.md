# Student Academic Success & Dropout Prediction

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

## 📌 Project Overview
This project aims to predict student academic outcomes (**Graduate** vs. **Dropout**) by analyzing a comprehensive dataset of demographic, socio-economic, and academic factors. By identifying "at-risk" students early, educational institutions can implement targeted interventions to improve retention rates.

**Dataset Source:** [Kaggle - Predict students' dropout and academic success](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention)

---

## 🛠️ Technical Workflow

### 1. Data Understanding & EDA
* **Exploratory Data Analysis:** Analyzed the distribution of features such as Marital Status, Course selection, and Scholarship status using Seaborn and Matplotlib.
* **Outlier Removal:** Used **Z-score analysis** to filter out statistical anomalies (Z > 3) to ensure data quality.
* **Feature Selection:** Categorized attributes into Demographic, Socio-economic, and Academic groups to better understand their correlation with student success.

### 2. Data Preparation & Engineering
* **Feature Consolidation:** Reduced noise by merging redundant features (e.g., combining Mother’s and Father’s qualifications into "Parents' Qualification").
* **Handling Class Imbalance:** Applied **SMOTE (Synthetic Minority Over-sampling Technique)** to balance the dataset, preventing the model from being biased toward the majority class.
* **Preprocessing:** Standardized numerical inputs using **MinMaxScaler** for optimal model performance.

### 3. Model Development & Evaluation
I evaluated four machine learning algorithms to find the most robust predictor:
* **Logistic Regression** (Selected Model)
* **K-Nearest Neighbors (KNN)**
* **Support Vector Machine (SVM)**
* **Decision Tree**

Each model was fine-tuned using **GridSearchCV** or **RandomizedSearchCV** to find the best hyperparameters.

---

## 📊 Results & Performance
The final **Logistic Regression** model was chosen for its high interpretability and balanced performance across Accuracy, Precision, Recall, and F1-Score.

| Model | Accuracy | F1-Score |
| :--- | :--- | :--- |
| Logistic Regression | 93.1% | 94.67% |
| KNN | 76.73% | 82.39% |
| SVM | 63.51 | 77.68% |
| Decision Tree | 86.39% | 89.34% |

---

## 🚀 Deployment
The final model is serialized using the `pickle` library. A functional CLI tool is included in the notebook to allow users to input real-time student data and receive a predicted outcome.

### Usage:
1. Clone this repository.
2. Run the Jupyter Notebook `Data Science Assignment .ipynb`.
3. Use the `main()` function to interact with the trained model.

---

## 👨‍💻 Author
**Boon Xiang** *Data Science (Honours) Graduate, TAR UMT* *Specializing in AI Foundations, Cloud Architecting, and Predictive Analytics.*

---
