# Exploratory Data Analysis (EDA) of the Titanic Dataset

This repository contains a Jupyter Notebook that performs a foundational Exploratory Data Analysis (EDA) on the classic Titanic dataset. The goal of this analysis is to understand the dataset's structure, identify potential data quality issues, and uncover initial insights through basic statistical inspection.

---
## Dataset

The analysis is performed on the `train.csv` file from the **Kaggle Titanic competition**. This dataset contains information about passengers on the Titanic, including whether they survived, their age, class, sex, and more.

---
## Key Analysis Questions Answered

The notebook walks through the following fundamental EDA steps to understand the data:

1.  **How big is the data?**: Checking the dimensions (rows and columns) using `.shape`.
2.  **How does the data look?**: Previewing random and initial rows using `.sample()` and `.head()`.
3.  **What is the data type of each column?**: Inspecting column data types and non-null counts with `.info()`.
4.  **Are there any missing values?**: Quantifying missing data points for each feature using `.isnull().sum()`.
5.  **What is the mathematical summary of the data?**: Generating descriptive statistics for numerical columns with `.describe()`.
6.  **Are there any duplicate rows?**: Checking for and counting duplicate entries using `.duplicated().sum()`.
7.  **How are the numerical features correlated?**: Calculating the correlation matrix with `.corr()` to see relationships between variables.

---
## Summary of Findings 📊

* **Dataset Size**: The dataset contains **891 rows** and **12 columns**.
* **Missing Data**: Significant missing values were found in the **`Age`** (177 missing), **`Cabin`** (687 missing), and **`Embarked`** (2 missing) columns.
* **Data Types**: The dataset contains a mix of numerical (`int64`, `float64`) and categorical (`object`) data.
* **Duplicates**: There are **no duplicate rows** in the dataset.
* **Correlation Highlights**: `Pclass` (Passenger Class) shows a notable negative correlation with `Survived`, suggesting that passengers in higher classes were more likely to survive.

---
## Technologies Used 💻
* **Python**
* **Pandas**
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone the repository to your local machine.
2.  Place the `train.csv` file in the root directory.
3.  Install the required libraries:
    ```bash
    pip install pandas jupyter
    ```
4.  Open and run the `understanding_data.ipynb` notebook to follow the analysis.
