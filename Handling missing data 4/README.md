# Advanced Techniques for Handling Missing Data

This project explores three advanced techniques for handling missing data in a machine learning workflow. The repository contains three Jupyter Notebooks, each providing a practical guide on a different method: **Random Sampling Imputation**, creating a **Missing Indicator Feature**, and building a **Custom Automated Imputer**.

---
## Datasets

The notebooks use two datasets:
* **Titanic Dataset (`train.csv`)**: Used for Random Sampling Imputation and Missing Indicator demonstrations.
* **House Prices Dataset (`house-train.csv`)**: Used for the Automatic Imputer Selection notebook.

---
## Missing Data Handling Methods

### 1. Random Sampling Imputation (`Random sampling imputation.ipynb`)
* **Concept**: This technique replaces missing values with a random sample of the observed values from the same feature. Its primary advantage is that it **preserves the original variance** of the feature, unlike mean/median imputation.
* **Implementation**: The notebook demonstrates how to build a custom function to perform random sampling imputation and uses KDE plots and variance checks to show its effectiveness in maintaining the original data distribution.

### 2. Missing Indicator (`Missing indicator.ipynb`)
* **Concept**: This technique adds a new binary feature to the dataset that indicates whether the data was missing for a given observation (1 for missing, 0 for not missing). This is useful when the fact that a value is missing is itself a predictive signal.
* **Implementation**: The notebook shows two ways to achieve this:
    * Using scikit-learn's `MissingIndicator` transformer.
    * Using the `add_indicator=True` parameter within `SimpleImputer`, which both imputes the original column and adds the indicator feature in one step.

### 3. Automatic Imputer Selection (`Automatically-select-imputer.ipynb`)
* **Concept**: This notebook tackles the challenge of applying different imputation strategies to different data types at scale. It demonstrates how to create a **custom scikit-learn transformer** that automatically detects whether a column is numerical or categorical.
* **Implementation**:
    * A custom class `Feature_imputer` is built, inheriting from scikit-learn's `BaseEstimator` and `TransformerMixin`.
    * The transformer is designed to apply **mean imputation** to numerical columns and **mode (most frequent) imputation** to categorical columns automatically.
    * This custom transformer can then be integrated into a larger `ColumnTransformer` pipeline for streamlined preprocessing.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**
* **Matplotlib** & **Seaborn**
* **scikit-learn**
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `train.csv` and `house-train.csv` files are in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib seaborn jupyter
    ```
4.  Open and run the Jupyter Notebooks to see each technique in action.
