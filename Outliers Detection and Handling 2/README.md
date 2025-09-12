# Outlier Detection and Handling Using the IQR Method

This project demonstrates how to identify and handle outliers using the **Interquartile Range (IQR) method**. The IQR method is a robust statistical technique for detecting outliers that is less sensitive to extreme values than the Z-score method, making it particularly effective for skewed datasets.

The notebook explores two common strategies for dealing with the identified outliers: **trimming** (removal) and **capping** (winsorizing).

---
## Dataset

The demonstration uses the `placement (1).csv` dataset, which contains student placement data. The analysis focuses on the skewed `placement_exam_marks` column.

---
## The IQR Method Explained ⚙️

The notebook follows these key steps to identify outliers:
1.  **Data Exploration**: The dataset is loaded, and the initial distributions are visualized using KDE plots and boxplots.
2.  **Calculate IQR**:
    * The 25th percentile (Q1) and 75th percentile (Q3) of the data are calculated.
    * The IQR is calculated as: `IQR = Q3 - Q1`.
3.  **Define Outlier Boundaries**: The boundaries for identifying outliers are established using the 1.5 * IQR rule:
    * **Upper Boundary**: `Q3 + 1.5 * IQR`
    * **Lower Boundary**: `Q1 - 1.5 * IQR`
4.  Any data point that falls outside these boundaries is considered an outlier.

---
## Trimming vs. Capping 📊

The notebook demonstrates two different approaches to handle the identified outliers:

* **1. Trimming (Removal)**: This method involves completely removing the rows that contain outlier values. It is a simple approach but can lead to a loss of data.
* **2. Capping (Winsorizing)**: This method involves replacing the outlier values with the calculated upper and lower boundary values. This retains the data points while reducing the skewing effect of the extreme values.

The notebook visually compares the "before and after" distributions for both methods, showing how each effectively deals with outliers.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation and calculation.
* **Seaborn** & **Matplotlib**: For data visualization (KDE plots, boxplots).
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `placement (1).csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy seaborn matplotlib jupyter
    ```
4.  Open and run the `IQR method.ipynb` notebook to see the outlier detection and handling processes.
