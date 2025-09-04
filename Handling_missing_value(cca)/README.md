# Handling Missing Data with Complete Case Analysis (CCA)

This project demonstrates **Complete Case Analysis (CCA)**, also known as listwise deletion, which is a straightforward method for handling missing data. The Jupyter Notebook shows how to apply this technique and, more importantly, how to analyze its impact on the dataset's original distributions.

CCA works by simply discarding all rows that contain one or more missing values. It operates under the assumption that the missing data is **Missing Completely At Random (MCAR)**.

---
## Dataset

The demonstration uses the Kaggle Titanic dataset (`train.csv`), which has missing values in the `Age`, `Cabin`, and `Embarked` columns.

---
## Process and Impact Analysis 📊

The notebook follows these steps:
1.  **Identify Missing Data**: Calculates and displays the percentage of missing values for each column.
2.  **Apply CCA**: Creates a new DataFrame by dropping all rows with `NaN` values using `df.dropna()`.
3.  **Analyze the Impact**: This is the crucial step where the notebook compares the original dataset with the CCA-processed dataset to check for potential bias:
    * **Numerical Features**: The distributions of `Age` and `Fare` are compared using histograms and KDE plots to see if they have significantly changed.
    * **Categorical Features**: The frequency distributions of `Sex`, `Embarked`, and `Pclass` are compared using count plots.

---
## Advantages & Disadvantages of CCA

* **Advantages**:
    * Simple and easy to implement.
    * Preserves the original variable distributions if the data is MCAR and only a small percentage of data is removed.

* **Disadvantages**:
    * Can lead to a significant loss of data, reducing the statistical power of the analysis.
    * Can introduce bias if the missing data is not MCAR, as the remaining data may no longer be representative of the original population.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**
* **Seaborn** & **Matplotlib**: For visualizing and comparing distributions.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `train.csv` file (from the Titanic dataset) is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy seaborn matplotlib jupyter
    ```
4.  Open and run the `complete_case_analysis.ipynb` notebook to see the method and its impact.
