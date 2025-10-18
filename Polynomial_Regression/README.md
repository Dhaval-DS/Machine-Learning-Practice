# Polynomial Regression for Non-Linear Data

This project demonstrates **Polynomial Regression**, a powerful technique used to model non-linear relationships between variables by fitting a linear model to a non-linear transformation of the features. The Jupyter Notebook provides a clear, step-by-step guide on how to generate polynomial features and train a linear regression model to fit a quadratic dataset.

---
## Dataset 📊

The demonstration uses a **synthetic dataset** generated with NumPy. The data is intentionally created to follow a quadratic relationship (`y = 0.8x² + 0.9x + 2`) with some added random noise, making it unsuitable for a simple linear regression model.

---
## Methodology & Workflow ⚙️

The notebook follows these key steps:
1.  **Data Generation**: Creates a non-linear dataset based on a quadratic equation.
2.  **Train-Test Split**: The data is split into training and testing sets.
3.  **Feature Transformation (`PolynomialFeatures`)**:
    * An instance of `PolynomialFeatures` from scikit-learn is used to transform the original feature `X` into polynomial features (e.g., `X` and `X²`). This is the core step that allows a linear model to learn a non-linear relationship.
4.  **Model Training**: A `LinearRegression` model is trained on the newly created polynomial features.
5.  **Evaluation**: The model's performance is evaluated using the R-squared (R²) score.
6.  **Pipeline Implementation**: The notebook also demonstrates how to streamline the entire process by chaining the `PolynomialFeatures` transformation and the `LinearRegression` model together using scikit-learn's **`Pipeline`** object.

---
## Visualization 📈

The notebook includes several visualizations to build a strong intuition for the process:
* A **2D scatter plot** shows the original non-linear data and the final fitted polynomial regression curve.
* An interactive **3D surface plot** created with **Plotly** visualizes the regression plane learned by the model when considering two input features, providing a clear picture of how the model fits the data in a higher-dimensional space.

---
## Technologies Used 💻
* **Python**
* **NumPy**: For data generation and numerical operations.
* **scikit-learn**: For `PolynomialFeatures`, `LinearRegression`, `Pipeline`, and `train_test_split`.
* **Matplotlib** & **Plotly**: For 2D and 3D data visualization.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Install the required libraries:
    ```bash
    pip install numpy scikit-learn matplotlib plotly jupyter
    ```
3.  Open and run the `Polynomial_Regression.ipynb` notebook to see the entire process and visualizations.
