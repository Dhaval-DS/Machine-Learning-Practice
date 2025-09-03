# Data Transformation with scikit-learn's PowerTransformer

This project demonstrates how to use scikit-learn's **`PowerTransformer`** to transform skewed numerical data into a more Gaussian-like (normal) distribution. This is a powerful preprocessing step that can stabilize variance and make data more suitable for machine learning models that assume normality.

---
## Dataset

The demonstration uses the `Age` and `Fare` columns from the Kaggle Titanic dataset (`train.csv`).

---
## Assessing Normality

The notebook uses two key visualization techniques to assess the normality of the data distributions before and after transformation:
* **Kernel Density Estimate (KDE) Plots**: To visually inspect the shape of the distribution.
* **Quantile-Quantile (Q-Q) Plots**: To compare the quantiles of the data distribution with the quantiles of a theoretical normal distribution. A straight line indicates a good fit.

---
## Transformation Methods Covered

The notebook explores the two main methods available in `PowerTransformer`:

### 1. Box-Cox Transform
* **Concept**: A statistical transformation that works only with **strictly positive data**. It finds the best `lambda` parameter to make the data as normal as possible.
* **Implementation**: The `PowerTransformer` is configured with `method='box-cox'` and applied to the dataset.

### 2. Yeo-Johnson Transform
* **Concept**: A more flexible transformation that works with data containing **zero and negative values**, in addition to positive values.
* **Implementation**: The `PowerTransformer` is used with its default setting, `method='yeo-johnson'`.

---
## Workflow

For both methods, the notebook follows the standard machine learning pipeline:
1.  Perform a train-test split.
2.  **Fit** the `PowerTransformer` **only on the training data** to learn the optimal transformation parameters (`lambdas`).
3.  **Transform** both the training and testing data using the fitted transformer to prevent data leakage.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data handling.
* **scikit-learn**: For `PowerTransformer` and `train_test_split`.
* **Seaborn** & **Matplotlib**: For data visualization.
* **SciPy**: For generating Q-Q plots.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `train.csv` file (from the Titanic dataset) is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib scipy jupyter
    ```
4.  Open and run the `power transformer.ipynb` notebook to see the transformations and their effects.
