# Custom Preprocessing with scikit-learn's FunctionTransformer

This project demonstrates how to use scikit-learn's **`FunctionTransformer`**, a flexible tool that allows you to integrate any custom Python function into a machine learning preprocessing pipeline. The notebook shows a practical example of applying a **logarithmic transformation** to a skewed feature to make its distribution more normal, which can improve the performance of many machine learning models.

---
## Dataset

The demonstration uses the `Age` and `Fare` columns from the Kaggle Titanic dataset (`train.csv`).

---
## Methodology & Pipeline

The Jupyter Notebook builds a custom preprocessing pipeline with the following steps:
1.  **Data Preparation**: The dataset is loaded, missing values are handled, and a train-test split is performed.
2.  **Initial Visualization**: The initial distribution of the `Fare` column is visualized using KDE plots to show its right-skewed nature.
3.  **Define Custom Function**: A function is created to apply a log transformation (`np.log1p`).
4.  **Create `FunctionTransformer`**: An instance of `FunctionTransformer` is created, wrapping the custom log transform function.
5.  **Integrate with `ColumnTransformer`**: A `ColumnTransformer` is used to selectively apply the `FunctionTransformer` only to the `Fare` column, while leaving the `Age` column unchanged (`remainder='passthrough'`).
6.  **Apply the Pipeline**: The complete transformation pipeline is fitted on the training data and then used to transform both the train and test sets.
7.  **Final Visualization**: The distribution of the transformed `Fare` column is plotted again to show that it is now less skewed and more Gaussian-like.

---
## Key Concepts Illustrated 💡

* Creating a **custom transformation function** (e.g., log transform).
* Wrapping the custom function in a **`FunctionTransformer`** to make it compatible with scikit-learn pipelines.
* Using **`ColumnTransformer`** to apply this custom transformer to specific columns of a dataset.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data handling and mathematical operations.
* **scikit-learn**: For `FunctionTransformer`, `ColumnTransformer`, and `train_test_split`.
* **Seaborn** & **Matplotlib**: For data visualization.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `train.csv` file (from the Titanic dataset) is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib jupyter
    ```
4.  Open and run the `function_transformer.ipynb` notebook to see the custom pipeline in action.
