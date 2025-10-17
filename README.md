# Implementing and Visualizing Variants of Gradient Descent

This project provides a detailed exploration of the three main variants of the **Gradient Descent** optimization algorithm: **Batch**, **Stochastic**, and **Mini-Batch Gradient Descent**. The repository contains several Jupyter Notebooks that not only implement these algorithms from scratch and with scikit-learn but also provide animated visualizations to build a strong intuition for how they work.

---
## Datasets 📊

The notebooks use two main datasets:
* **Diabetes Dataset**: A real-world dataset from scikit-learn used for the multiple linear regression implementations.
* **Synthetic Regression Dataset**: A simple dataset generated with `make_regression` for creating the animated visualizations.

---
## Variants of Gradient Descent

### 1. Batch Gradient Descent (`Batch_Gradient_Descent.ipynb`)
* **Concept**: In Batch Gradient Descent, the model's parameters are updated by calculating the gradient of the loss function using the **entire training dataset** in each epoch. This provides a stable convergence but can be computationally expensive for large datasets.
* **Implementation**: The notebook implements a custom `BGDRegressor` class from scratch and compares its performance with scikit-learn's standard `LinearRegression` model.

### 2. Stochastic Gradient Descent (SGD) (`stiochastic Gradient Descent.ipynb`)
* **Concept**: In SGD, the model's parameters are updated after calculating the gradient on **just one randomly selected training sample** at a time. This is much faster per update and can escape local minima, but the convergence path is noisy and less stable.
* **Implementation**: The notebook implements a custom `SGDRegressor` class and also demonstrates how to use scikit-learn's `SGDRegressor` for comparison.

### 3. Mini-Batch Gradient Descent (`Mini_batch Gradient Descent.ipynb`)
* **Concept**: Mini-Batch GD is a compromise between Batch and Stochastic GD. It updates the model's parameters after calculating the gradient on a **small, random batch of training samples**. This balances the stability of Batch GD with the speed of SGD.
* **Implementation**: The notebook implements a `MBGDRegressor` class from scratch that processes the data in mini-batches over several epochs.

---
## Animated Visualizations (`stochastic-gradient-descent-animation.ipynb`) 🎥

To provide a clear intuition of the optimization process, this notebook creates several animated visualizations for Stochastic Gradient Descent:

* **Line Plot Animation**: Shows the regression line adjusting its fit with each data point it processes.
* **Cost Plot Animation**: Visualizes how the cost (loss) decreases over time as the model learns.
* **Contour Plot Animation**: Shows the path the algorithm takes on a 2D contour plot of the loss function as it moves towards the optimal values for the slope (`m`) and intercept (`b`). A similar plot is also available for Mini-Batch GD.

---
## Technologies Used 💻
* **Python**
* **NumPy**: For numerical operations.
* **scikit-learn**: For datasets and model comparison.
* **Matplotlib**: For plotting and creating animations.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Install the required libraries:
    ```bash
    pip install numpy scikit-learn matplotlib
    ```
3.  Open and run the Jupyter Notebooks to explore each Gradient Descent variant and its visualization.
