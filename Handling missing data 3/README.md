# Handling Missing Categorical Data: Frequent Value & Missing Category Imputation

This project explores two common techniques for handling missing **categorical data**: **Frequent Value (Mode) Imputation** and **Missing Category Imputation**. The repository contains two Jupyter Notebooks, each providing a practical guide on how to apply these methods using scikit-learn's `SimpleImputer` and how to analyze their impact on the feature's distribution.

---
## Dataset

Both demonstrations use the `Train.csv` dataset, focusing on the categorical feature `BsmtQual` (Basement Quality), which contains missing values.

---
## Imputation Methods for Categorical Features

### 1. Frequent Value (Mode) Imputation (`frequent value imputation .ipynb`)
* **Concept**: This technique replaces missing values in a categorical column with the **most frequent value (mode)** of that column. It's a simple method but can distort the original frequency distribution by over-representing the mode.
* **Implementation**: The notebook demonstrates how to:
    * Use scikit-learn's `SimpleImputer` with `strategy='most_frequent'`.
    * Fit the imputer on the **training set only** to learn the mode and prevent data leakage.
    * Transform both the training and test sets with the learned mode.
    * Visualize the impact on the feature's distribution using bar plots.

### 2. Missing Category Imputation (`missing category imputation.ipynb`)
* **Concept**: This technique involves replacing missing values with a **new, constant value** (e.g., 'Missing' or 'Unknown'). This is useful when the fact that a value is missing is itself important information, as it effectively creates a new, distinct category.
* **Implementation**: The notebook shows how to:
    * Use `SimpleImputer` with `strategy='constant'` and a specified `fill_value`.
    * Apply the imputer to both the training and testing sets.
    * Visualize the impact, which shows the creation of the new "Missing" category in the bar plot.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**
* **Matplotlib**: For data visualization.
* **scikit-learn**: For `train_test_split` and `SimpleImputer`.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `Train.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib jupyter
    ```
4.  Open and run the `frequent value imputation .ipynb` and `missing category imputation.ipynb` notebooks to see each technique in action.
