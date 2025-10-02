# Evaluating Regression Model Performance with Key Metrics

This project provides a practical guide to evaluating the performance of a regression model using several standard metrics. The Jupyter Notebook demonstrates how to train a Simple Linear Regression model and then calculate and interpret key performance indicators to understand the model's accuracy and effectiveness.

---
## Dataset 📊

The demonstration uses the `placement.csv` dataset, where the goal is to predict a student's `package` (salary package) based on their `cgpa`.

---
## Regression Metrics Covered ⚙️

The notebook implements and explains the following essential regression metrics from scikit-learn:

* **Mean Absolute Error (MAE)**: Calculates the average of the absolute differences between the predicted and actual values. It gives an idea of the magnitude of the error but not the direction.

* **Mean Squared Error (MSE)**: Calculates the average of the squared differences between predicted and actual values. It penalizes larger errors more heavily than smaller ones.

* **Root Mean Squared Error (RMSE)**: The square root of the MSE. It brings the error metric back to the same unit as the target variable, making it more interpretable.

* **R-squared (R²)**: Also known as the coefficient of determination, it represents the proportion of the variance in the dependent variable that is predictable from the independent variable(s). It ranges from 0 to 1, with higher values indicating a better fit.

* **Adjusted R-squared**: A modified version of R-squared that adjusts for the number of predictors in the model. It is particularly useful for multiple linear regression, as it penalizes the addition of irrelevant features.

---
## Workflow

1.  **Data Preparation**: The `placement.csv` dataset is loaded and split into training and testing sets.
2.  **Model Training**: A `LinearRegression` model is trained on the `cgpa` (feature) to predict the `package` (target).
3.  **Metric Calculation**: The trained model makes predictions on the test set, and each of the metrics listed above is calculated by comparing the predicted values to the actual values.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation.
* **scikit-learn**: For `LinearRegression`, `train_test_split`, and all metric functions (`mean_absolute_error`, `r2_score`, etc.).
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
4.  Open and run the `Regression_metrics.ipynb` notebook to see the model evaluation process.
