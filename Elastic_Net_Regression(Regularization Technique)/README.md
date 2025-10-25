# Elastic Net Regression: The Best of L1 and L2 Regularization

This project demonstrates **Elastic Net Regression**, a sophisticated regularization technique that combines the penalties of both **Lasso (L1)** and **Ridge (L2)** regression. This hybrid approach allows Elastic Net to inherit the best properties of both: it can shrink coefficients like Ridge and also perform automatic feature selection by setting some coefficients to exactly zero, like Lasso.

---
## Dataset & Model Comparison 📊

The notebook uses the `load_diabetes` dataset from scikit-learn to compare the performance of four different regression models on the same data:

1.  **Linear Regression** (No Regularization)
2.  **Ridge Regression** (L2 Penalty)
3.  **Lasso Regression** (L1 Penalty)
4.  **Elastic Net Regression** (L1 + L2 Penalty)

---
## Workflow ⚙️

1.  **Data Preparation**: The `load_diabetes` dataset is loaded and split into training and testing sets.
2.  **Model Training**: Each of the four models (`LinearRegression`, `Ridge`, `Lasso`, `ElasticNet`) is trained on the same training data.
3.  **Performance Evaluation**: The **R-squared (R²)** score is calculated for each model on the test set, providing a direct, quantitative comparison of their predictive performance.

This notebook effectively demonstrates how Elastic Net functions as a powerful alternative that can outperform both Ridge and Lasso, especially in datasets with high dimensionality or multicollinearity.

---
## Technologies Used 💻
* **Python**
* **scikit-learn**: For datasets (`load_diabetes`), models (`LinearRegression`, `Ridge`, `Lasso`, `ElasticNet`), and metrics (`r2_score`, `train_test_split`).
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Install the required libraries:
    ```bash
    pip install scikit-learn jupyter
    ```
3.  Open and run the `Elastic_Net_Regression.ipynb` notebook to see the model comparison.
