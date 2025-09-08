# Advanced Imputation with scikit-learn's IterativeImputer (MICE)

This project provides an in-depth guide to **Multivariate Imputation by Chained Equations (MICE)**, a sophisticated method for handling missing data, implemented in scikit-learn as **`IterativeImputer`**. Unlike simpler methods, MICE models each feature with missing values as a function of other features, making it a powerful tool for creating accurate imputations.

---
## Dataset

This notebook demonstrates the MICE technique, which can be applied to datasets like the **`50_Startups.csv`** file. This dataset includes numerical features like `R&D Spend`, `Administration`, and `Marketing Spend`.

**Note**: While the provided `50_Startups.csv` file is complete, this notebook's technique is designed for datasets *with* missing values in such numerical columns.

---
## The MICE Algorithm ⚙️

The MICE algorithm implemented by `IterativeImputer` works as follows:
1.  **Initial Fill**: A simple imputation (like the mean) is used to temporarily fill all missing values.
2.  **Round-Robin Regression**:
    * One feature column with missing values is selected as the target variable (`y`).
    * All other features are used as predictors (`X`).
    * A regression model is trained on the rows where the target variable was not originally missing.
    * The model predicts the missing values, and they are updated.
3.  **Iteration**: This process is repeated for each column with missing values, constituting one cycle. Multiple cycles are performed, with the imputations from one cycle being used as predictors in the next, until the imputed values stabilize.

---
## Implementation in the Notebook

The `MICE-iterative imputer.ipynb` notebook shows how to set up and apply the `IterativeImputer` from scikit-learn to a dataset. It follows the standard workflow of splitting data into training and testing sets, fitting the imputer on the training data, and then transforming both sets to prevent data leakage.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**
* **scikit-learn**: For `IterativeImputer`, `LinearRegression`, etc.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure your dataset (e.g., a version of `50_Startups.csv` with missing values) is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn jupyter
    ```
4.  Open and run the `MICE-iterative imputer.ipynb` notebook to see the imputation process in action.
