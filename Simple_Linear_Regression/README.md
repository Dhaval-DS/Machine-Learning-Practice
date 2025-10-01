# Simple Linear Regression: From Scratch and with scikit-learn

This project provides a comprehensive look at **Simple Linear Regression**, demonstrating how to build a predictive model from two different perspectives:
1.  **From Scratch**: By creating a custom Python class that implements the underlying mathematical formulas of Ordinary Least Squares (OLS).
2.  **Using scikit-learn**: By leveraging the powerful, pre-built `LinearRegression` model from the scikit-learn library.

---
## Dataset 📊

Both demonstrations use the `placement.csv` dataset, which contains student data. The goal is to predict a student's `package` (salary package) based on their `cgpa`.

---
## Implementations

### 1. Simple Linear Regression From Scratch (`Simple_linear_regression(own class).ipynb`)
* **Concept**: This notebook demystifies the mechanics of linear regression by building a custom class named `MyLR`.
* **Methodology**:
    * The `fit()` method calculates the slope (`m`) and intercept (`b`) of the regression line using the OLS mathematical formulas directly.
    * The `predict()` method uses the calculated `m` and `b` to make predictions on new data.
    * The notebook concludes by plotting the resulting regression line over the data points.

### 2. Simple Linear Regression with scikit-learn (`Simple_Linear_Regression.ipynb`)
* **Concept**: This notebook shows the standard, efficient way to implement linear regression in a machine learning workflow using a popular library.
* **Methodology**:
    * The data is split into training and testing sets.
    * An instance of scikit-learn's `LinearRegression` class is created and trained on the data using the `.fit()` method.
    * The model's learned coefficients (`coef_`) and intercept (`intercept_`) are inspected.
    * Predictions are made on the test data, and the resulting regression line is visualized.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation.
* **scikit-learn**: For the `LinearRegression` model and `train_test_split`.
* **Matplotlib**: For data visualization.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `placement.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib jupyter
    ```
4.  Open and run both the `Simple_linear_regression(own class).ipynb` and `Simple_Linear_Regression.ipynb` notebooks to see each implementation.
