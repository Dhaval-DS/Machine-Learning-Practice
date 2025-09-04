# Feature Engineering: Handling Mixed Variables

This project demonstrates a common feature engineering technique: **handling mixed variables**. Mixed variables are features that contain both numerical and categorical information within a single column (e.g., a ticket number like 'SC/PARIS 2149' or a cabin number like 'C85').

This notebook shows how to parse such a column and separate it into two new, distinct features: one categorical and one numerical. This process makes the data more usable for machine learning algorithms.

---
## Dataset

The demonstration likely uses a dataset like the Kaggle Titanic dataset, which contains mixed variable columns such as `Cabin` and `Ticket`.

---
## Methodology: Separating Mixed Features

The notebook illustrates a step-by-step process to extract meaningful information from a mixed variable column:

1.  **Identify the Mixed Variable**: A column containing both string and number components is identified.
2.  **Define Extraction Logic**: Custom logic, potentially using string manipulation or regular expressions, is created to isolate the categorical and numerical parts.
3.  **Create New Categorical Feature**: The extracted string/categorical part is placed into a new column.
4.  **Create New Numerical Feature**: The extracted numerical part is placed into a second new column and converted to a numerical data type.
5.  **Drop Original Column**: The original mixed variable column is often dropped to avoid redundancy.

### Example (using the `Cabin` column)
* **Original Column `Cabin`**: `'C85'`
* **New Categorical Column `Cabin_Letter`**: `'C'`
* **New Numerical Column `Cabin_Number`**: `85`

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation and extraction.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the required dataset is in the same directory.
3.  Install the necessary libraries:
    ```bash
    pip install pandas numpy jupyter
    ```
4.  Open and run the Jupyter Notebook to see the feature engineering process in action.# Feature Engineering: Handling Mixed Variables

This project demonstrates a common feature engineering technique: **handling mixed variables**. Mixed variables are features that contain both numerical and categorical information within a single column (e.g., a ticket number like 'SC/PARIS 2149' or a cabin number like 'C85').

This notebook shows how to parse such a column and separate it into two new, distinct features: one categorical and one numerical. This process makes the data more usable for machine learning algorithms.

---
## Dataset

The demonstration likely uses a dataset like the Kaggle Titanic dataset, which contains mixed variable columns such as `Cabin` and `Ticket`.

---
## Methodology: Separating Mixed Features

The notebook illustrates a step-by-step process to extract meaningful information from a mixed variable column:

1.  **Identify the Mixed Variable**: A column containing both string and number components is identified.
2.  **Define Extraction Logic**: Custom logic, potentially using string manipulation or regular expressions, is created to isolate the categorical and numerical parts.
3.  **Create New Categorical Feature**: The extracted string/categorical part is placed into a new column.
4.  **Create New Numerical Feature**: The extracted numerical part is placed into a second new column and converted to a numerical data type.
5.  **Drop Original Column**: The original mixed variable column is often dropped to avoid redundancy.

### Example (using the `Cabin` column)
* **Original Column `Cabin`**: `'C85'`
* **New Categorical Column `Cabin_Letter`**: `'C'`
* **New Numerical Column `Cabin_Number`**: `85`

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation and extraction.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the required dataset is in the same directory.
3.  Install the necessary libraries:
    ```bash
    pip install pandas numpy jupyter
    ```
4.  Open and run the Jupyter Notebook to see the feature engineering process in action.
