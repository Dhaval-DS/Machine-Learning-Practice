# Univariate Exploratory Data Analysis (EDA) on the Titanic Dataset

This repository contains a Jupyter Notebook focused on **Univariate Analysis**, a fundamental step in Exploratory Data Analysis (EDA). The notebook examines individual features of the Titanic dataset to understand their distributions, central tendencies, and spreads.

---
## Dataset

The analysis is performed on the `train.csv` file from the **Kaggle Titanic competition**, which contains demographic and travel information for passengers aboard the Titanic.

---
## Analysis of Individual Features

The notebook is divided into two main sections based on the type of data being analyzed:

### 1. Categorical Data Analysis
This section focuses on understanding the frequency and proportions of different categories within a feature. The following visualizations are used:

* **`Countplot`**: To visualize the number of passengers from each port of embarkation (`Embarked`).
* **`Pie Chart`**: To show the percentage distribution of passengers who survived versus those who did not (`Survived`).

### 2. Numerical Data Analysis
This section explores the distribution and statistical properties of numerical features, primarily focusing on the `Age` of the passengers. The techniques include:

* **`Histogram`**: To visualize the frequency distribution of passenger ages.
* **`Displot`**: To create a smoothed distribution curve (KDE) over a histogram, providing a clearer view of the age distribution.
* **`Boxplot`**: To identify the median, quartiles, and potential outliers in the `Age` data.
* **Descriptive Statistics**: Calculating key metrics like `.min()`, `.max()`, `.mean()`, and `.skew()` to mathematically summarize the `Age` column.

---
## Technologies Used 💻
* **Python**
* **Pandas**: For data loading and manipulation.
* **Seaborn** & **Matplotlib**: For data visualization.
* **Jupyter Notebook**: As the development environment.

---
## How to Use This Repository

1.  Clone the repository to your local machine.
2.  Place the `train.csv` dataset in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas seaborn matplotlib jupyter
    ```
4.  Open and run the `EDA(univariate).ipynb` notebook to see the analysis and visualizations.
