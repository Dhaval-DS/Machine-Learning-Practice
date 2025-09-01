# One-Hot Encoding for Categorical Data

This project demonstrates **One-Hot Encoding (OHE)**, a standard method for converting nominal categorical data into a numerical format that can be used by machine learning algorithms. The Jupyter Notebook explores three different approaches to applying OHE using both the **pandas** and **scikit-learn** libraries.

---
## Dataset

The demonstration uses the `cars.csv` dataset, which includes nominal categorical features like `brand`, `fuel`, and `owner`.

---
## Key Techniques Covered

The notebook provides a hands-on guide to three common OHE workflows:

### 1. One-Hot Encoding with pandas (`pd.get_dummies`)
* **Concept**: A quick and straightforward method for applying OHE directly to a DataFrame.
* **Implementation**: Uses the `pd.get_dummies()` function and shows how to use the `drop_first=True` parameter to prevent multicollinearity.

### 2. One-Hot Encoding with scikit-learn on a Train-Test Split
* **Concept**: The standard machine learning approach. The encoder is fitted **only on the training data** to prevent data leakage and then used to transform both the training and testing sets.
* **Implementation**: Uses `train_test_split` and scikit-learn's `OneHotEncoder`.

### 3. One-Hot Encoding with Top Categories
* **Concept**: A practical technique for handling **high-cardinality features** (categorical variables with many unique values). This method involves encoding only the most frequent categories and grouping the rest into a single "other" category.
* **Implementation**: Identifies the top N categories using `value_counts()` and then applies OHE to the modified feature.

---
## Technologies Used 💻
* **Python**
* **Pandas**: For data loading and using `get_dummies`.
* **scikit-learn**: For `OneHotEncoder` and `train_test_split`.
* **NumPy**
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `cars.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas scikit-learn numpy jupyter
    ```
4.  Open and run the `one_hot_encoding.ipynb` notebook to see the different methods in action.
