# Dimensionality Reduction with PCA on the Digit Recognizer Dataset

This project demonstrates **Principal Component Analysis (PCA)**, a powerful dimensionality reduction technique used to transform a high-dimensional dataset into a smaller, more manageable set of uncorrelated variables called principal components. The goal is to reduce the number of features while retaining most of the original data's variance.

The Jupyter Notebook provides a practical application of PCA on the popular **Digit Recognizer dataset** from Kaggle.

---
## Dataset 🖼️

The analysis uses the `train.csv` file from the Kaggle Digit Recognizer competition.
* It contains thousands of grayscale images of hand-written digits (0-9).
* Each image is **28x28 pixels**, flattened into a single row with **784 pixel features** (plus a 'label' column).
* The high dimensionality (784 features) makes it an excellent candidate for PCA.

---
## Methodology and Workflow ⚙️

The notebook follows these key steps to apply PCA:
1.  **Data Loading**: The dataset is loaded into a pandas DataFrame, separating the features (pixels) from the target (labels).
2.  **Data Scaling (`StandardScaler`)**: The pixel values are standardized to have a mean of 0 and a standard deviation of 1. This is a crucial step, as PCA is sensitive to the scale of the features.
3.  **Applying PCA**:
    * An instance of `PCA` from scikit-learn is created.
    * The PCA model is **fitted** to the scaled training data to learn the principal components.
4.  **Analyzing Explained Variance**:
    * The notebook plots the **cumulative explained variance** to determine the optimal number of principal components needed to capture a significant portion (e.g., 95%) of the dataset's variance.
5.  **Dimensionality Reduction**: Based on the analysis, a new PCA model is created with the chosen number of components, and the original data is transformed into this new, lower-dimensional space.

---
## Key Outcome

By applying PCA, the original 784-dimensional dataset is successfully reduced to a much smaller number of principal components while retaining the vast majority of the information, making it more efficient for training machine learning models.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation.
* **scikit-learn**: For `StandardScaler` and `PCA`.
* **Matplotlib**: For data visualization.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `train.csv` file is in the `Data_extraction_technique(PCA)` directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy scikit-learn matplotlib jupyter
    ```
4.  Open and run the `pca-practice-on-digit-recognizer-dataset.ipynb` notebook to see the dimensionality reduction process.
