# 🧊 Titanic Survival Analysis & Machine Learning Prediction

<div align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/6/6e/Titanic_%281912%29_3.jpg" width="500"/>
</div>

---

## 📌 Overview

This project is an end-to-end data science case study on the Titanic dataset. It includes:

- 📊 **Exploratory Data Analysis (EDA)**
- 🧹 **Data Preprocessing**
- 🧠 **Supervised Machine Learning**
- 📈 **Model Evaluation and Comparison**

Our objective is to build a model that predicts whether a passenger survived the Titanic disaster using demographic and passenger information.

---

## 📂 Dataset

The dataset comes from the [Kaggle Titanic competition](https://www.kaggle.com/competitions/titanic). It contains information such as:

| Column | Description |
|--------|-------------|
| `Pclass` | Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd) |
| `Sex` | Gender |
| `Age` | Age in years |
| `SibSp` | # of siblings/spouses aboard |
| `Parch` | # of parents/children aboard |
| `Fare` | Ticket fare |
| `Embarked` | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |
| `Survived` | Survival (0 = No, 1 = Yes) – *Target Variable* |

---

## 🔍 Exploratory Data Analysis

The EDA involved:

- 🔎 Visualizing survival distribution across **gender**, **class**, **age**, **fare**, and **embarkation**
- 🧱 Handling missing values (`Age`, `Embarked`, `Cabin`)
- 🧠 Feature engineering: family size, binary encoding, removing noise
- 📊 Visuals: Histograms, bar plots, box plots, heatmaps

### Key Insights:

- 👩‍🦰 Women had significantly higher survival rates than men  
- 💰 Passengers in 1st class were more likely to survive  
- 👶 Children and young adults had better chances of survival  
- ⚓ Embarkation point had mild influence on survival probability  

---

## ⚙️ Preprocessing Steps

- Imputed missing values:
  - `Age`: Median imputation
  - `Embarked`: Mode imputation
- Dropped columns: `Cabin`, `Ticket`, `Name`, `PassengerId`
- Categorical encoding with `get_dummies`
- Feature scaling using `StandardScaler`

---

## 🧠 Machine Learning Models

### 📌 Logistic Regression
- **Accuracy:** 80.45%
- **F1 Score (Survived):** 0.72

### 📌 Random Forest Classifier
- **Accuracy:** 81.01%
- **F1 Score (Survived):** 0.74

| Metric     | Logistic Regression | Random Forest |
|------------|---------------------|---------------|
| Accuracy   | 80.45%              | 81.01%        |
| Precision  | 0.79                | 0.79          |
| Recall     | 0.67                | 0.70          |
| F1-Score   | 0.72                | 0.74          |

✅ Random Forest shows slightly better performance and recall on the positive class (survivors).

---

## 🛠️ Tech Stack

- **Language:** Python 3.x
- **IDE:** Jupyter Notebook
- **Libraries:** 
  - `pandas`, `numpy` for data manipulation  
  - `seaborn`, `matplotlib` for visualization  
  - `scikit-learn` for modeling, preprocessing, and metrics
