# Data Standardization with scikit-learn's StandardScaler

This project demonstrates **Standardization**, a crucial data preprocessing technique in machine learning. The Jupyter Notebook shows how to use scikit-learn's `StandardScaler` to transform numerical features to have a **mean of 0** and a **standard deviation of 1**. This process is often necessary for machine learning algorithms that are sensitive to the scale of input features.

---
## Dataset

The demonstration uses a subset of the Kaggle Titanic dataset (`train.csv`), focusing on the numerical columns: `Pclass`, `Age`, and `Fare`.

---
## Methodology

The notebook follows these key steps:
1.  **Load Data**: The Titanic dataset is loaded, and relevant numerical columns are selected.
2.  **Handle Missing Values**: Missing values in the `Age` column are imputed with the mean.
3.  **Initial Visualization**: `Seaborn`'s Kernel Density Estimate (KDE) plots are used to visualize the original distributions of the `Age` and `Fare` columns.
4.  **Apply StandardScaler**:
    * An instance of `StandardScaler` is created.
    * The scaler is fitted and applied to the data using the `.fit_transform()` method.
5.  **Analyze Transformed Data**: The resulting scaled data is examined to confirm that the mean is approximately 0 and the standard deviation is 1 for each feature.
6.  **Final Visualization**: KDE plots are generated again for the transformed `Age` and `Fare` columns to visually show the effect of standardization.

---
## Key Results 📊

The notebook clearly illustrates that after applying `StandardScaler`:
* The **mean** of each feature is scaled to a value very close to **0**.
* The **standard deviation** of each feature is scaled to **1**.
* The **shape of the original distribution** is preserved, but the data is centered at zero.

---
## Technologies Used 💻
* **Python**
* **Pandas**: For data handling.
* **scikit-learn**: For applying the `StandardScaler`.
* **Seaborn** & **Matplotlib**: For data visualization.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Place the `train.csv` dataset in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas scikit-learn seaborn matplotlib jupyter
    ```
4.  Open and run the `standardization.ipynb` notebook to see the entire process and its results.
