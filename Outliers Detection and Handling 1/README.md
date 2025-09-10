# Outlier Detection and Removal Using Z-score

This project demonstrates how to identify and remove outliers from a dataset using the **Z-score method**. The Z-score measures how many standard deviations a data point is from the mean. A common threshold for identifying outliers is a Z-score greater than 3 or less than -3 (the 3-sigma rule). This notebook provides a step-by-step guide to applying this technique.

---
## Dataset

The demonstration uses the `placement (1).csv` dataset, which contains student placement data. The analysis focuses on the `cgpa` and `placement_exam_marks` columns.

---
## Step-by-Step Process ⚙️

The notebook follows these key steps:
1.  **Data Exploration**: The dataset is loaded, and the initial distributions of the features are visualized using KDE plots and boxplots to identify potential outliers.
2.  **Calculate Z-scores**: A new column is created containing the Z-score for each data point in the `cgpa` feature. The formula used is `z = (x - mean) / std`.
3.  **Identify and Filter Outliers**: The code identifies and then removes all rows where the absolute Z-score of the `cgpa` is greater than 3.
4.  **Compare Results**: The notebook compares the "before and after" datasets by:
    * Checking the change in the shape of the DataFrame.
    * Visualizing the new distributions with KDE plots and boxplots to confirm that the outliers have been removed.

---
## Key Results 📊

* The notebook successfully identifies data points that are more than 3 standard deviations from the mean in the `cgpa` column.
* After removing these outliers, the new boxplot and distribution plots show a cleaner, more condensed data range without the extreme values.

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
4.  Open and run the `outliers remover using z-score.ipynb` notebook to see the outlier detection process.
