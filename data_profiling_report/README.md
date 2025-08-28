# Automated EDA with Pandas Profiling (ydata-profiling)

This project demonstrates the power of automated Exploratory Data Analysis (EDA) using the **`ydata-profiling`** library (formerly known as `pandas-profiling`). The goal is to generate a comprehensive, interactive data profile report from a dataset with minimal code.

---
## Dataset

The analysis is performed on the `train.csv` file from the Kaggle Titanic competition, which contains passenger information.

---
## Methodology

The Jupyter Notebook (`Pandas_Profilling.ipynb`) follows a simple three-step process:
1.  Loads the Titanic dataset into a DataFrame using **`pandas`**.
2.  Initializes a **`ProfileReport`** object from the DataFrame.
3.  Generates and saves the complete analysis to an interactive HTML file named **`output.html`**.

---
## The Interactive Report (`output.html`) 📊

The main output of this project is the **`output.html`** file, which is an interactive EDA report. It provides a deep dive into the dataset, including:

* **Overview**: High-level statistics about the dataset (variables, observations, missing values).
* **Variable Analysis**: In-depth univariate analysis for each column with distributions, statistics, and more.
* **Interaction Plots**: Bivariate analysis to explore relationships between variables.
* **Correlation Matrix**: Heatmaps showing correlations between numerical features.
* **Missing Value Analysis**: Visualizations of missing data patterns.
* **Data Sample**: A preview of the first and last rows of the dataset.

---
## Technologies Used 💻
* **Python**
* **Pandas**: For data loading.
* **ydata-profiling** (formerly `pandas-profiling`): For automated EDA report generation.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Place the `train.csv` dataset in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas ydata-profiling jupyter
    ```
4.  Run the `Pandas_Profilling.ipynb` notebook to regenerate the report.
5.  Open the **`output.html`** file in your browser to view the interactive EDA report.
