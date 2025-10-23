# Lasso Regression (L1 Regularization): Overfitting Control and Feature Selection

This project provides a comprehensive guide to **Lasso Regression (L1 Regularization)**, a powerful technique used to improve linear models by preventing overfitting and performing automatic feature selection.

Lasso (Least Absolute Shrinkage and Selection Operator) works by adding a penalty to the loss function proportional to the **absolute value of the coefficients**. This has two key effects:
1.  It **shrinks coefficients** towards zero, which helps prevent overfitting.
2.  It can shrink some coefficients **exactly to zero**, effectively removing irrelevant features from the model.

---
## Datasets 📊

* **Diabetes Dataset**: A real-world, multivariate dataset from scikit-learn used to demonstrate Lasso's effect on coefficients.
* **Synthetic Datasets**: Simple 1D and 2D datasets are generated to visualize Lasso's impact on fitting a curve.

---
## Project Components ⚙️

### 1. Lasso for Controlling Overfitting (`lasso_Regression .ipynb`)
* **Concept**: This notebook demonstrates how Lasso can be used to control the complexity of a high-degree **Polynomial Regression** model, preventing it from overfitting to the training data.
* **Methodology**:
    * A `Pipeline` is created that combines `PolynomialFeatures` (degree 16) with a `Lasso` model.
    * The notebook visualizes how increasing the regularization strength (`alpha`) forces the overly complex polynomial curve to become simpler and smoother, resulting in a more generalized model.

### 2. Lasso for Feature Selection (`Lasso_Regression_key_understanding.ipynb`)
* **Concept**: This notebook provides a deep dive into Lasso's most famous property: its ability to perform **automatic feature selection**.
* **Methodology**:
    * Lasso models are trained on the `load_diabetes` dataset using a wide range of `alpha` values.
    * The notebook plots the "Lasso Path"—the magnitude of each feature's coefficient as a function of `alpha`. This clearly shows that as `alpha` increases, many coefficients are forced to **exactly zero**, effectively removing them from the model.

---
## Technologies Used 💻
* **Python**
* **NumPy** & **Pandas**: For data manipulation.
* **scikit-learn**: For `Lasso`, `PolynomialFeatures`, `Pipeline`, `make_regression`, `load_diabetes`, and `train_test_split`.
* **Matplotlib**: For all data visualizations.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib jupyter
    ```
3.  Open and run the Jupyter Notebooks to explore each concept in detail.
