# Bivariate & Multivariate EDA on the Titanic Dataset

This repository contains a Jupyter Notebook that performs **Bivariate and Multivariate Exploratory Data Analysis (EDA)** on the Titanic dataset. The analysis aims to uncover relationships, patterns, and correlations between different pairs and groups of features.

---
## Dataset

The analysis uses the `train.csv` file from the Kaggle Titanic competition, which contains passenger information from the Titanic.

---
## Exploring Relationships Between Features

The notebook demonstrates how to analyze the interaction between variables using various visualization techniques:

### 1. Bivariate Analysis (Analyzing two variables at a time)

* **Categorical vs. Numerical Data:**
    * **`Boxplot`**: Used to compare the distribution of a numerical variable (like `Age`) across different categories (like `Survived`).
    * **`Barplot`**: Used to visualize the relationship between a categorical variable (`Pclass`) and the central tendency of a numerical variable (`Fare`).

* **Numerical vs. Numerical Data:**
    * **`Scatterplot`**: Used to examine the relationship between two continuous variables (e.g., `Age` vs. `Fare`).

* **Categorical vs. Categorical Data:**
    * **`Heatmap` on a Contingency Table (`crosstab`)**: Used to visualize the frequency distribution between two categorical variables (e.g., `Pclass` vs. `Survived`).

### 2. Multivariate Analysis (Analyzing more than two variables)

* **Enhanced `Scatterplot`**: Using `hue` and `style` parameters to encode additional categorical variables into a scatterplot, allowing for the visualization of relationships between multiple variables at once (e.g., plotting `Age` vs. `Fare` while coloring by `Survived` and using different marker styles for `Pclass`).
* **`Heatmap` on a Correlation Matrix**: Provides a concise visual summary of the correlations between all numerical variables in the dataset.

---
## Technologies Used 💻
* **Python**
* **Pandas**: For data manipulation and creating contingency tables.
* **Seaborn** & **Matplotlib**: For advanced data visualization.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Place the `train.csv` dataset in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas seaborn matplotlib jupyter
    ```
4.  Open and run the `EDA(Bivariate and Multivariate).ipynb` notebook to see the analysis.
