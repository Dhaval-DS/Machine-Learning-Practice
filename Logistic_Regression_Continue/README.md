# Advanced Logistic Regression: Softmax, Polynomials, and Visualization

This collection of files explores advanced concepts in Logistic Regression, moving beyond simple binary classification. It includes implementations of **Softmax Regression** for multi-class problems, **Polynomial Logistic Regression** for non-linear decision boundaries, and an interactive **Streamlit** tool for visualizing these concepts.

---
## Components ⚙️

### 1. Softmax Regression Demo (`softmax_regression_demo.ipynb`)
* **Objective**: To demonstrate multi-class classification using Logistic Regression (Softmax Regression).
* **Dataset**: The classic **Iris dataset**, loaded via Seaborn.
* **Methodology**:
    * The target variable `species` (Setosa, Versicolor, Virginica) is label-encoded.
    * A `LogisticRegression` model is initialized with `multi_class='multinomial'`, enabling the **Softmax** function for probability estimation across multiple classes instead of the standard sigmoid function.
    * The model is trained on a subset of features (`sepal_length`, `petal_length`) to predict the flower species.

### 2. Polynomial Logistic Regression (`polynomial-logistic-regression.ipynb`)
* **Objective**: To classify data that is not linearly separable by transforming features.
* **Dataset**: A synthetic dataset (`ushape.csv`) that likely contains data points arranged in a U-shape or similar non-linear pattern.
* **Methodology**:
    * **Linear Attempt**: First, a standard linear Logistic Regression model is trained. The visualization using `mlxtend`'s `plot_decision_regions` shows that a straight line fails to separate the classes effectively.
    * **Polynomial Transformation**: The notebook then introduces `PolynomialFeatures` (degree 3) to create new, higher-order features from the original data.
    * **Non-Linear Boundary**: By fitting Logistic Regression on these transformed features, the model can learn a curved decision boundary that fits the non-linear data much better.

### 3. Streamlit Visualization Tool (`streamlit-viz-tool.py`)
* **Objective**: A Python script designed to create an interactive web application using **Streamlit**.
* **Features**:
    * Allows users to select between **Binary** (2 clusters) and **Multiclass** (3 clusters) datasets generated using `make_blobs`.
    * Uses standard `LogisticRegression` to fit the data.
    * **Visualizes Decision Boundaries**: It generates a meshgrid over the feature space to plot the decision boundaries and regions colored by class predictions, providing a dynamic way to understand how the classifier partitions the space.

---
## Technologies Used 💻
* **Python**
* **Scikit-learn**: For model implementation (`LogisticRegression`), data generation (`make_blobs`), and preprocessing (`LabelEncoder`, `PolynomialFeatures`).
* **Pandas & NumPy**: For data handling.
* **Matplotlib & Seaborn**: For static plotting and dataset loading.
* **Mlxtend**: For plotting decision regions.
* **Streamlit**: For creating the interactive visualization web app.

---
## How to Run

1.  **Notebooks**: Open `softmax_regression_demo.ipynb` or `polynomial-logistic-regression.ipynb` in Jupyter to run the static demos.
2.  **Streamlit App**: Run the visualization tool from your terminal:
    ```bash
    streamlit run streamlit-viz-tool.py
    ```
