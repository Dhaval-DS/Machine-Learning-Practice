# Categorical Data Encoding: Ordinal vs. Label Encoding

This project demonstrates two common techniques for converting categorical data into a numerical format suitable for machine learning algorithms: **Ordinal Encoding** and **Label Encoding**. The Jupyter Notebook provides a clear, step-by-step implementation of both methods using scikit-learn.

---
## Dataset

The demonstration uses a sample `customer.csv` dataset, which includes both ordinal categorical features (`review`, `education`) and a nominal target variable (`purchased`).

---
## Encoding Techniques Covered

The notebook covers the following encoding methods:

### 1. Ordinal Encoding (`OrdinalEncoder`)
* **When to Use**: This technique is used for **ordinal features**, which are categorical variables with a clear, intrinsic order (e.g., `Poor` < `Average` < `Good`).
* **Implementation**:
    * The `OrdinalEncoder` from scikit-learn is used.
    * A specific order for the categories is defined to ensure the encoding reflects the feature's rank.
    * The encoder is applied to the independent features (`review` and `education`).

### 2. Label Encoding (`LabelEncoder`)
* **When to Use**: This technique is typically used for encoding the **target variable (`y`)**. It converts a single column of categorical labels into numerical labels (0, 1, 2, etc.). It's generally not recommended for independent features if there is no inherent order, as it can mislead some ML models.
* **Implementation**:
    * The `LabelEncoder` from scikit-learn is used.
    * The encoder is applied to the `purchased` column.

---
## Technologies Used 💻
* **Python**
* **Pandas**: For data loading and manipulation.
* **scikit-learn**: For applying `OrdinalEncoder` and `LabelEncoder`.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `customer.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas scikit-learn jupyter
    ```
4.  Open and run the `Ordinal and Label Encoding.ipynb` notebook to see the implementation of both encoding techniques.
