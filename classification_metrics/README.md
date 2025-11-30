# Mastering Classification Metrics: Binary and Multi-Class

This project provides a practical guide to evaluating classification models using a wide array of performance metrics. The repository contains three Jupyter Notebooks that cover **Binary Classification** and **Multi-Class Classification** scenarios, using both **Logistic Regression** and **Decision Tree Classifiers** to demonstrate how different metrics behave.

---
## Datasets 📊

The notebooks utilize three distinct datasets to illustrate different classification challenges:
* **Binary Dataset**: A binary classification dataset (loaded from CSV) used to introduce fundamental metrics.
* **Iris Dataset**: A classic multi-class dataset with 3 classes (Setosa, Versicolor, Virginica), ideal for understanding metrics beyond simple yes/no predictions.
* **MNIST Dataset**: A complex multi-class dataset of handwritten digits (0-9), used to demonstrate how metrics scale to 10 different classes.

---
## Project Components ⚙️

### 1. Binary Classification Metrics (`classificationmetrics-binary.ipynb`)
* **Objective**: To evaluate model performance on a two-class problem.
* **Models**: `LogisticRegression` vs. `DecisionTreeClassifier`.
* **Key Metrics Implemented**:
    * **Accuracy Score**: The overall percentage of correct predictions.
    * **Confusion Matrix**: A breakdown of True Positives, True Negatives, False Positives, and False Negatives.
    * **Precision, Recall, and F1-Score**: Calculated to provide a more nuanced view of model performance, especially for imbalanced data.

### 2. Multi-Class Metrics with Iris (`classificationmetrics-multi-iris1.ipynb`)
* **Objective**: To extend classification metrics to a 3-class problem.
* **Methodology**:
    * The target labels are encoded using `LabelEncoder`.
    * Both **Logistic Regression** and **Decision Trees** are trained and compared.
* **Key Concepts**:
    * **Multi-Class Confusion Matrix**: Visualizing misclassifications across 3 classes.
    * **Precision & Recall with `average=None`**: Calculating metrics for each class individually to identify specific weaknesses.

### 3. Multi-Class Metrics with MNIST (`classificationmetrics-multi-mnist1.ipynb`)
* **Objective**: To apply metrics to a larger, 10-class problem (Digit Recognition).
* **Methodology**:
    * Splits the MNIST data into training and testing sets.
    * Trains `LogisticRegression` and `DecisionTreeClassifier` on pixel data.
* **Key Metrics**:
    * **10x10 Confusion Matrix**: A detailed view of which digits are confused with others.
    * **Classification Report**: A comprehensive summary table showing Precision, Recall, F1-Score, and Support for all 10 digits at once.

---
## Technologies Used 💻
* **Python**
* **Pandas**: For data manipulation and DataFrame creation.
* **scikit-learn**:
    * **Models**: `LogisticRegression`, `DecisionTreeClassifier`
    * **Metrics**: `accuracy_score`, `confusion_matrix`, `precision_score`, `recall_score`, `f1_score`, `classification_report`
    * **Preprocessing**: `LabelEncoder`, `train_test_split`
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Install the required libraries:
    ```bash
    pip install pandas scikit-learn
    ```
3.  Open the notebooks to see the direct comparison between Logistic Regression and Decision Trees across different datasets.
