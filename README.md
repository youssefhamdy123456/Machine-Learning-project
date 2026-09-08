# 💰 Adult Census Income Classification

A Machine Learning classification project that predicts whether a person's annual income is **greater than $50K or less than or equal to $50K** based on demographic, educational, occupational, and financial features.

The project focuses on data preprocessing, exploratory data analysis, feature encoding, feature scaling, and comparing multiple Machine Learning classification algorithms.

---

## 📌 Project Overview

The goal of this project is to build a Machine Learning model capable of predicting an individual's income category from Census data.

The target variable is:

```text
income
```

with two possible classes:

```text
<=50K
>50K
```

Several classification algorithms were trained and evaluated to determine which model provides the best performance.

---

## 📊 Dataset

The dataset contains **32,561 records** and **15 columns**.

### Features

| Feature          | Description                           |
| ---------------- | ------------------------------------- |
| `age`            | Age of the person                     |
| `workclass`      | Type of employer                      |
| `fnlwgt`         | Statistical weight                    |
| `education`      | Education level                       |
| `education.num`  | Numerical representation of education |
| `marital.status` | Marital status                        |
| `occupation`     | Type of occupation                    |
| `relationship`   | Family relationship                   |
| `race`           | Race                                  |
| `sex`            | Gender                                |
| `capital.gain`   | Capital gains                         |
| `capital.loss`   | Capital losses                        |
| `hours.per.week` | Working hours per week                |
| `native.country` | Country of origin                     |
| `income`         | Target variable                       |

---

## 🔄 Machine Learning Workflow

```text
Raw Dataset
     │
     ▼
Data Loading
     │
     ▼
Data Inspection
     │
     ├── Shape
     ├── Info
     ├── Statistics
     └── Missing Values
     │
     ▼
Remove Duplicates
     │
     ▼
Train / Test Split
     │
     ▼
Missing Value Imputation
     │
     ▼
Exploratory Data Analysis
     │
     ▼
Feature Selection
     │
     ▼
Label Encoding
     │
     ▼
Standard Scaling
     │
     ▼
Model Training
     │
     ├── Logistic Regression
     ├── Decision Tree
     ├── Random Forest
     └── KNN
     │
     ▼
Model Evaluation
     │
     ▼
Model Comparison
```

---

## 🧹 Data Preprocessing

Several preprocessing steps were performed before training the models.

### 1. Remove Duplicates

Duplicate records were identified and removed from the dataset.

### 2. Train/Test Split

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**

Stratified splitting was used to preserve the target class distribution.

```python
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    shuffle=True,
    random_state=15,
    stratify=y
)
```

### 3. Missing Values

Missing values were found in:

* `occupation`
* `workclass`
* `native.country`

They were handled using `SimpleImputer` with the **most frequent** strategy.

### 4. Feature Selection

The following features were removed:

```text
education
native.country
```

### 5. Categorical Encoding

Categorical features were converted into numerical values using **Label Encoding**.

### 6. Feature Scaling

`StandardScaler` was applied to scale the numerical features before model training.

---

## 🔍 Exploratory Data Analysis

The project includes several visualizations to understand the relationships between features and income.

The analysis includes:

* Income class distribution
* Age vs. working hours
* Capital gain distribution
* Education and income relationship
* Gender and income relationship
* Race and income relationship
* Native country distribution
* Feature correlation heatmap

---

## 🤖 Machine Learning Models

Four classification algorithms were implemented and compared.

### 1. Logistic Regression

```text
Accuracy: 82.16%
```

### 2. Decision Tree

```text
Accuracy: 81.04%
```

### 3. Random Forest

```text
Accuracy: 85.88%
```

### 4. K-Nearest Neighbors (KNN)

```text
Accuracy: 82.94%
```

---

## 📈 Model Comparison

| Model               |   Accuracy |
| ------------------- | ---------: |
| Logistic Regression |     82.16% |
| Decision Tree       |     81.04% |
| KNN                 |     82.94% |
| **Random Forest**   | **85.88%** |

### 🏆 Best Model

**Random Forest Classifier** achieved the highest accuracy among the tested models:

> **85.88% Test Accuracy**

Random Forest also achieved an F1-score of:

* `<=50K` → **0.91**
* `>50K` → **0.68**

This shows that the model performs better overall at identifying the `<=50K` class, while the `>50K` class remains more challenging to classify.

---

## 📊 Random Forest Classification Report

| Class        | Precision | Recall | F1-Score |
| ------------ | --------: | -----: | -------: |
| `<=50K`      |      0.89 |   0.93 |     0.91 |
| `>50K`       |      0.75 |   0.62 |     0.68 |
| **Accuracy** |           |        | **0.86** |

---

## 🧪 Evaluation Metrics

The models were evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Correlation Analysis

---

## 🛠️ Technologies Used

* Python
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook / Google Colab

### Machine Learning Algorithms

* Logistic Regression
* Decision Tree
* Random Forest
* K-Nearest Neighbors

### Preprocessing Techniques

* Simple Imputation
* Label Encoding
* Standard Scaling
* Train/Test Split

---

## 📁 Project Structure

```text
Adult-Census-Income-Classification/
│
├── Adult_Census_Income.ipynb
├── README.md
└── requirements.txt
```

> The original dataset is not included in the repository because the local copy is no longer available.

---

## ▶️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/youssefhamdy123456/Adult-Census-Income-Classification.git
```

### 2. Install Dependencies

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### 3. Open the Notebook

Open:

```text
Adult_Census_Income.ipynb
```

using Jupyter Notebook or Google Colab.

### 4. Add the Dataset

The notebook expects the dataset file:

```text
Adult Census Income.csv
```

Place the dataset in the appropriate working directory before running the notebook.

### 5. Run the Notebook

Execute the cells sequentially to reproduce the preprocessing, analysis, model training, and evaluation.

---

## ⚠️ Dataset Availability

The dataset used in the original project is **not included in this repository** because the original local copy was lost.

However, the notebook documents the expected dataset structure and preprocessing workflow.

---

## 🎯 Project Objectives

* Understand Census Income data
* Perform Exploratory Data Analysis
* Handle missing values
* Remove duplicate records
* Encode categorical variables
* Apply feature scaling
* Train multiple classification models
* Compare model performance
* Select the best-performing model
* Evaluate predictions using multiple metrics

---

## 👨‍💻 Author

**Youssef Diab**

AI & Machine Learning Engineer

GitHub:
https://github.com/youssefhamdy123456

---

## ⭐ Project Highlights

* ✅ Binary Classification
* ✅ Exploratory Data Analysis
* ✅ Missing Value Handling
* ✅ Duplicate Removal
* ✅ Label Encoding
* ✅ Standard Scaling
* ✅ Multiple ML Algorithms
* ✅ Model Comparison
* ✅ Confusion Matrix
* ✅ Classification Report
* ✅ Random Forest — **85.88% Accuracy**
