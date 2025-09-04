# Data Discretization: Binarization and Binning

This project explores two key data preprocessing techniques for discretizing continuous numerical features: **Binarization** and **Binning**. The repository contains two Jupyter Notebooks, each providing a practical guide on how to apply these methods using scikit-learn to prepare data for machine learning models.

---
## Dataset

Both demonstrations use the Kaggle Titanic dataset (`train.csv`).

---
## Discretization Methods

### 1. Binarization (`binarization.ipynb`)
* **Concept**: Binarization is the process of converting a numerical feature into a binary (0 or 1) feature based on a specified threshold. It's useful for creating boolean flags from continuous or count data.
* **Implementation**: The notebook demonstrates how to use scikit-learn's **`Binarizer`** within a `ColumnTransformer` to create a new feature indicating whether a passenger was traveling alone or with family.

### 2. Binning (`binning.ipynb`)
* **Concept**: Binning (or discretization) is the process of converting continuous numerical features into discrete categorical bins. This can help some models handle non-linear relationships and reduce the impact of outliers.
* **Implementation**: The notebook uses scikit-learn's **`KBinsDiscretizer`** to demonstrate three different binning strategies:
    * **Uniform Binning (`strategy='uniform'`)**: Creates bins of equal width across the range of the data.
    * **Quantile Binning (`strategy='quantile'`)**: Creates bins with an equal number of data points in each.
    * **K-Means Binning (`strategy='kmeans'`)**: Creates bins based on the clusters found by the K-Means algorithm.

---
## Workflow

Both notebooks follow the standard machine learning pipeline: performing a train-test split, fitting the transformer **only on the training data**, and then transforming both the training and testing sets to prevent data leakage.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**
* **scikit-learn** (for `Binarizer`, `KBinsDiscretizer`, `ColumnTransformer`, etc.)
* **Seaborn** & **Matplotlib**
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `train.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn seaborn matplotlib jupyter
    ```
4.  Open and run the `binarization.ipynb` and `binning.ipynb` notebooks to see each technique in action.
