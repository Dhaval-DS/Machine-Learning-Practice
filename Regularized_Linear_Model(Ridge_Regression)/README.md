# A Comprehensive Guide to Ridge Regression (L2 Regularization)

This project provides a multi-faceted exploration of **Ridge Regression (L2 Regularization)**, a fundamental technique used to combat overfitting and multicollinearity in linear models. The repository contains five Jupyter Notebooks that cover the topic from foundational concepts to advanced, from-scratch implementations.

The project demonstrates:
* The core concept of L2 regularization and its effect on model coefficients.
* How Ridge Regression prevents overfitting in Polynomial Regression.
* Building Ridge Regression from scratch for 2D data (Simple Linear Regression).
* Building a multivariate Ridge regressor from scratch using the **closed-form solution**.
* Building a multivariate Ridge regressor from scratch using **Gradient Descent**.

---
## Datasets 📊

* **Diabetes Dataset**: Used for the multivariate regression examples.
* **Synthetic 2D Dataset**: Generated with `make_regression` for the simple linear regression implementation.

---
## Core Concepts and Implementations ⚙️

### 1. Conceptual Understanding & Visualization
* **`Ridge_Regularization.ipynb`**: This notebook demonstrates how Ridge Regression helps prevent **overfitting** in a high-degree **Polynomial Regression** model. By adding a penalty for large coefficients, it forces the model to learn a simpler, smoother, and more generalized function. It visualizes how different values of the `alpha` parameter control the trade-off between bias and variance.
* **`ridge-regression-key-understandings.ipynb`**: This notebook provides a deep dive into the **effect of `alpha`** on the model's coefficients. It trains Ridge models with various `alpha` values and plots the coefficients, clearly showing that as `alpha` increases, the magnitude of all coefficients is **shrunk towards zero** (but not exactly to zero), which is the key mechanism of L2 regularization.

### 2. Implementation from Scratch: 2D Case
* **`ridge-regression-from-scratch-m-and-b for 2D.ipynb`**: This notebook builds a Ridge regressor from scratch specifically for the **simple linear regression** case (2D). It implements a custom class (`My_ridge`) that calculates the optimal slope (`m`) and intercept (`b`) using the modified Ordinary Least Squares (OLS) formulas that directly incorporate the `alpha` penalty term.

### 3. Implementation from Scratch: Multivariate (Closed-Form)
* **`ridge-regression-from-scratch.ipynb`**: This notebook implements a `Ridge` class for **multivariate data**. The `fit` method is built using the **closed-form (Normal Equation)** solution for Ridge Regression. This involves solving the equation:
    `weights = (X^T*X + alpha*I)^-1 * X^T*y`
    where `I` is the identity matrix and `alpha` is the regularization parameter.

### 4. Implementation from Scratch: Multivariate (Gradient Descent)
* **`ridge-regression-gradient-descent.ipynb`**: This notebook provides an alternative from-scratch implementation of a multivariate Ridge regressor (`My_RidgeGD`) using **Gradient Descent**. The `fit` method iteratively updates the model's coefficients by calculating the gradient of the modified loss function, which now includes the derivative of the L2 penalty term (`lambda * sum(weights^2)`).

---
## Technologies Used 💻
* **Python**
* **NumPy** & **Pandas**: For numerical operations and data manipulation.
* **scikit-learn**: For datasets, `LinearRegression`, `Ridge`, and `PolynomialFeatures`.
* **Matplotlib**: For all data visualizations.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib jupyter
    ```
3.  Open and run the Jupyter Notebooks to explore each concept and implementation in detail.
