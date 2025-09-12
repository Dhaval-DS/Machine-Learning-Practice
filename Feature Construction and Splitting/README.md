# Feature Engineering on the Titanic Dataset: Splitting and Construction

This project demonstrates two powerful **feature engineering** techniques—**Feature Splitting** and **Feature Construction**—applied to the classic Titanic dataset. The Jupyter Notebook provides a practical guide on how to create new, more meaningful features from existing ones, which can significantly improve the performance of machine learning models.

---
## Dataset

The techniques in this notebook are demonstrated in the context of the Kaggle Titanic dataset (`train.csv`).

---
## Key Techniques with Titanic Examples 🚀

### 1. Feature Splitting
* **Concept**: Feature Splitting is the process of breaking down a single, complex feature into multiple, simpler features.
* **Example on Titanic Data**: The notebook would show how to split the `Name` column to extract passenger titles (e.g., "Mr.", "Miss.", "Mrs.", "Master"). This new "Title" feature can be more predictive of survival than the full name.

### 2. Feature Construction
* **Concept**: Feature Construction is the process of creating new features by combining or transforming existing ones.
* **Example on Titanic Data**: The notebook would demonstrate how to create a new `Family_Size` feature by adding the `SibSp` (siblings/spouses aboard) and `Parch` (parents/children aboard) columns together. From this, another feature like `Is_Alone` could be constructed.

---
## Key Outcome

By applying these techniques, complex string data is simplified, and new relational features are created, making the dataset more suitable for machine learning algorithms.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation and feature creation.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the Titanic `train.csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy jupyter
    ```
4.  Open and run the `feature construction and splitting.ipynb` notebook to see the feature engineering process.
