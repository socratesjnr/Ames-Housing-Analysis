# 🏡 Ames Housing Data Analysis

This project focuses on performing a comprehensive **data cleaning and exploratory data analysis (EDA)** on the popular **Ames Housing Dataset**. The main goal was to prepare the dataset for machine learning tasks by handling missing values, identifying outliers, correcting data types, and engineering features.

> **Tool Used:** Python (Pandas, NumPy, Matplotlib, Seaborn, Statsmodels)  
> **Dataset Source:** [Ames Housing Dataset on Kaggle](https://www.kaggle.com/datasets/shashanknecrothapa/ames-housing-dataset)
> **Metadata and Documentation:** [Documentation Link](https://jse.amstat.org/v19n3/decock/DataDocumentation.txt)
---

## 📌 Objectives

- 🧼 Load and explore the Ames Housing dataset.
- 🔍 Identify and remove outliers.
- 🧮 Detect and handle missing values.
- 🔁 Transform and format categorical and numerical features.
- 📊 Prepare the dataset for further statistical analysis or machine learning modeling.

---

## 🔄 Workflow Overview

### 1. **Data Loading & Initial Inspection**
- Loaded the dataset using `pandas.read_csv()`.
- Displayed dataset structure with `.info()`, `.shape`, `.head()`, and `.tail()`.
- Used `.describe()` to get basic statistics of the numerical features.

### 2. **Outlier Detection**
- Noticed five unusual sales records with large `Gr Liv Area` (> 4000 sq ft).
- Removed those outliers to avoid bias in further analysis.

### 3. **Data Type Fixes**
- Converted `MSSubClass` from integer to string (e.g., "20" → "MSC20") for categorical interpretation.

### 4. **Missing Value Treatment**
- Identified missing values using:
  - `.isnull().sum()`  
  - Percentage of missing values per column
- Dropped columns with over **50% missing values**.
- Handled remaining missing data using appropriate strategies:
  - Replacing with `'None'` for nominal columns
  - Using mode/median for ordinal and numerical columns
  - Correlating `Garage Type` and `Garage Area` to infer missing values

### 5. **Feature Engineering**
- Created helper functions to automate repetitive fill-replace tasks.
- Standardized column formats (e.g., added dollar symbols, removed decimals).

---

## 🧠 Key Insights

- Some homes had unusual values (extremely high square footage and low prices) that skewed the dataset — removed them for better modeling accuracy.
- Many columns had missing values that were not random — requiring different treatment strategies for categorical vs numerical data.
- Converting numerical codes to categorical strings (like `MSSubClass`) improves interpretability and modeling outcomes.
- A cleaner, more structured dataset was achieved, ready for downstream tasks like regression modeling or classification.

---

## 🧰 Technologies Used

| Tool         | Purpose                             |
|--------------|-------------------------------------|
| **Pandas**   | Data manipulation & cleaning        |
| **NumPy**    | Numerical computation               |
| **Matplotlib / Seaborn** | Data visualization     |
| **Statsmodels** | Optional statistical analysis    |

---

---

## ✅ Next Steps

This project was focused on **cleaning and exploring** the dataset. Future improvements might include:

- Training a regression model (e.g., Linear Regression, XGBoost)
- Using pipelines to automate preprocessing
- Hyperparameter tuning and evaluation

---

## 📁 Repository Structure
```
Ames Housing Analysis/
├── Ames Housing Analysis.ipynb  # Jupyter Notebook with full analysis
├── dataset_data.csv             # Original dataset
└── README.md                    # Project documentation
```









---

## 🙋🏽‍♂️ About Me

I’m a data enthusiast exploring how real-world problems can be solved with clean, thoughtful, and purposeful data. This project is part of my growing portfolio as I transition into data science from a background in guidance and counseling — blending **human understanding with analytical power**.

📬 **Let’s connect!**  
- LinkedIn: [[My Profile](https://linkedin.com](https://www.linkedin.com/in/oluwaseyiadaramola/))  
- Email: oluwaseyitadaramola@gmail.com

---

> ⭐ If you liked this project, feel free to fork it, leave a ⭐️, or reach out with suggestions!
