# Streamlined Preprocessing with scikit-learn's ColumnTransformer

This project demonstrates how to use scikit-learn's **`ColumnTransformer`**, a powerful tool for applying different preprocessing steps to different columns of a dataset in a single, streamlined pipeline. This is essential for building robust machine learning models, as it ensures that the same transformations are applied consistently to both training and testing data.

---
## Dataset

The demonstration uses a subset of the Kaggle Titanic dataset (`train.csv`), focusing on a mix of numerical (`age`, `fare`) and categorical (`gender`, `embarked`) features.

---
## Methodology & Pipeline

The Jupyter Notebook builds a preprocessing pipeline with the following steps:
1.  **Data Preparation**: The dataset is loaded, and a train-test split is performed.
2.  **Define Transformers**:
    * An **`OneHotEncoder`** is set up to transform the categorical columns (`gender`, `embarked`).
    * The numerical columns (`age`, `fare`) are designated to be passed through without any transformation.
3.  **Construct `ColumnTransformer`**:
    * An instance of `ColumnTransformer` is created.
    * It is configured to apply the `OneHotEncoder` to the specified categorical columns.
    * The **`remainder='passthrough'`** argument is used to ensure that all other columns are kept in the final output.
4.  **Apply the Pipeline**:
    * The `ColumnTransformer` is **fitted and transformed** on the **training data** (`X_train`).
    * The fitted transformer is then used to **transform** the **testing data** (`X_test`), preventing data leakage.

---
## Key Concepts Illustrated 💡

* Applying different transformers to different columns within a single object.
* Using **`remainder='passthrough'`** to keep columns that don't need transformation.
* Setting **`handle_unknown='ignore'`** in the `OneHotEncoder` to gracefully handle categories that might appear in the test set but not in the training set.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data handling.
* **scikit-learn**: For `ColumnTransformer`, `OneHotEncoder`, and `train_test_split`.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `train.csv` file (from the Titanic dataset) is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn jupyter
    ```
4.  Open and run the `column_transformer.ipynb` notebook to see the pipeline in action.
