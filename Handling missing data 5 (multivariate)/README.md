# Advanced Imputation with scikit-learn's KNNImputer

This project demonstrates an advanced technique for handling missing numerical data using scikit-learn's **`KNNImputer`**. Unlike simple methods like mean or median imputation, the K-Nearest Neighbors (KNN) imputer predicts missing values based on the values of the 'k' nearest neighbors in the feature space. This often results in more accurate imputations as it considers the relationships between features.

---
## Dataset

The demonstration uses a subset of the Kaggle Titanic dataset (`train.csv`), focusing on the numerical features `Age`, `Fare`, and `Pclass`.

---
## Imputation and Evaluation Process ⚙️

The notebook follows these steps:
1.  **Data Preparation**: The dataset is loaded and split into training and testing sets.
2.  **Initialize `KNNImputer`**: An instance of `KNNImputer` is created with key parameters:
    * **`n_neighbors`**: The number of neighboring samples to use for imputation.
    * **`weights='distance'`**: Specifies that closer neighbors will have a greater influence on the imputation than neighbors that are further away.
3.  **Apply the Imputer**:
    * The imputer is **fitted** on the **training data** to learn the relationships between features.
    * Both the training and testing sets are then **transformed** using the fitted imputer.
4.  **Evaluate Impact on Model Performance**: To measure the effectiveness of the imputation, a `LogisticRegression` model is trained on the imputed data. The model's accuracy is then calculated on the transformed test set, providing a quantitative measure of how well the imputation strategy works in a predictive modeling context.

---
## Key Concepts Illustrated 💡

* Using a multivariate approach (`KNNImputer`) to impute missing values by considering other features.
* The importance of fitting imputers **only on the training data** to prevent data leakage.
* Evaluating the quality of an imputation strategy by measuring its impact on the performance of a downstream machine learning model.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**
* **scikit-learn**: For `KNNImputer`, `train_test_split`, `LogisticRegression`.
* **Seaborn** & **Matplotlib**
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `train.csv` file (from the Titanic dataset) is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib jupyter
    ```
4.  Open and run the `KNN imputer.ipynb` notebook to see the entire process.
