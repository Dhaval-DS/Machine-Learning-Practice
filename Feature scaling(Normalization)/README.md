# Data Normalization with scikit-learn's MinMaxScaler

This project demonstrates **Normalization** (specifically Min-Max Scaling), a common data preprocessing technique used in machine learning. The Jupyter Notebook shows how to use scikit-learn's `MinMaxScaler` to rescale numerical features into a fixed range, typically **between 0 and 1**. This is particularly useful for algorithms that do not assume any specific distribution of the data, such as K-Nearest Neighbors (KNN) and neural networks.

---
## Dataset

The demonstration uses the **Wine dataset** (`wine_data.csv`), focusing on the numerical columns `Proline`, `Alcohol`, and `Malic acid` to illustrate the scaling effect on features with different ranges.

---
## Methodology

The notebook follows these key steps:
1.  **Load Data**: The Wine dataset is loaded into a pandas DataFrame.
2.  **Initial Visualization**: `Seaborn`'s Kernel Density Estimate (KDE) plots and `scatterplots` are used to visualize the original distributions and relationships of the features, highlighting their different scales.
3.  **Apply MinMaxScaler**:
    * An instance of `MinMaxScaler` is created.
    * The scaler is fitted and applied to the data using the `.fit_transform()` method.
4.  **Create a Scaled DataFrame**: The transformed NumPy array is converted back into a pandas DataFrame for easier inspection and plotting.
5.  **Final Visualization**: KDE plots and scatterplots are generated again for the transformed features to visually confirm that all data now falls within the [0, 1] range while preserving the original shape of the distribution.

---
## Key Results 📊

The notebook clearly shows that after applying `MinMaxScaler`:
* All features are rescaled to a common range of **[0, 1]**.
* The **shape of the original distribution** for each feature is maintained.
* The **relative relationships** between data points are preserved, as seen in the before-and-after scatterplots.

---
## Technologies Used 💻
* **Python**
* **Pandas**: For data handling.
* **scikit-learn**: For applying the `MinMaxScaler`.
* **Seaborn** & **Matplotlib**: For data visualization.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `wine_data.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas scikit-learn seaborn matplotlib jupyter
    ```
4.  Open and run the `Normalization.ipynb` notebook to see the process and visualizations.
