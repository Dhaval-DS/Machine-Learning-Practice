# Outlier Removal Using the Percentile Method

This project demonstrates how to handle outliers by **trimming** (removing) them based on their **percentile rank**. This method involves defining a lower and upper percentile boundary (e.g., the 1st and 99th percentiles) and removing any data points that fall outside this range. It is a straightforward and effective way to deal with extreme values in a dataset.

---
## Dataset

The demonstration uses the `weight-height.csv` dataset, which contains height and weight data. The analysis focuses on removing outliers from the `height` column.

---
## Step-by-Step Process ⚙️

The notebook follows these key steps:
1.  **Data Exploration**: The dataset is loaded, and the initial distribution of the `height` feature is visualized using KDE plots and boxplots to identify the presence of extreme values.
2.  **Define Percentile Boundaries**:
    * The **upper limit** is set at the **99th percentile**.
    * The **lower limit** is set at the **1st percentile**.
3.  **Filter Outliers**: A new DataFrame is created by removing all rows where the `height` is either above the upper limit or below the lower limit.
4.  **Compare Results**: The notebook compares the "before and after" datasets by:
    * Checking the change in the shape of the DataFrame to see how many rows were removed.
    * Visualizing the new distribution with KDE plots and boxplots to confirm that the extreme outliers have been trimmed.

---
## Key Results 📊

* The notebook successfully removes the top 1% and bottom 1% of the data from the `height` column.
* The "after" visualizations show a cleaner distribution and a boxplot with a more condensed range, confirming the removal of the outliers.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation and calculation.
* **Seaborn** & **Matplotlib**: For data visualization (KDE plots, boxplots).
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `weight-height.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy seaborn matplotlib jupyter
    ```
4.  Open and run the `percentile method.ipynb` notebook to see the outlier removal process.
