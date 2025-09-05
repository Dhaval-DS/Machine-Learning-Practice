# Handling Missing Data: Mean, Median, and Arbitrary Value Imputation

This project explores two common techniques for handling missing numerical data: **Mean/Median Imputation** and **Arbitrary Value Imputation**. The repository contains two Jupyter Notebooks, each providing a practical guide on how to apply these methods and analyze their impact on the data's distribution.

---
## Dataset

Both demonstrations use the `titanic_toy.csv` dataset, which contains missing values in the `Age` column.

---
## Missing Value Imputation Methods

### 1. Mean/Median Imputation (`mean-median imputation.ipynb`)
* **Concept**: This technique replaces missing values in a numerical column with either the **mean** or the **median** of that column. It is a simple and fast method, but it can distort the original variance of the data by compressing it.
* **Implementation**: The notebook demonstrates how to:
    * Calculate the mean/median from the **training set only** to prevent data leakage.
    * Apply the calculated value to fill missing data in both the training and test sets.
    * Visualize the impact on the feature's distribution using KDE plots.

### 2. Arbitrary Value Imputation (`arbitrary-value-imputation.ipynb`)
* **Concept**: This technique involves replacing missing values with a fixed, arbitrary number that is not typically present in the data (e.g., 99, -1, or 999). This can be useful if the fact that a value was missing is important information in itself, as it effectively creates a new category for "missing".
* **Implementation**: The notebook shows how to:
    * Fill `NaN` values with an arbitrary number.
    * Visualize the impact on the feature's distribution using histograms, which clearly shows a new, distinct bar appearing at the arbitrary value.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**
* **Matplotlib**: For data visualization.
* **scikit-learn**: For `train_test_split`.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `titanic_toy.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib jupyter
    ```
4.  Open and run the `mean-median imputation.ipynb` and `arbitrary-value-imputation.ipynb` notebooks to see each technique in action.
