# Feature Engineering: Feature Splitting and Construction

This project demonstrates two powerful **feature engineering** techniques: **Feature Splitting** and **Feature Construction**. The Jupyter Notebook provides a practical guide on how to create new, more meaningful features from existing ones in a dataset, which can significantly improve the performance of machine learning models.

---
## Dataset

The demonstration uses a flight price prediction dataset (`Train (2).csv`), which contains features like flight `Route` and `Dep_Time` that are suitable for these techniques.

---
## Feature Engineering Techniques 🚀

### 1. Feature Splitting
* **Concept**: Feature Splitting is the process of breaking down a single, complex feature into multiple, simpler features. This is often done with strings that contain delimiters or structured information.
* **Implementation**: The notebook demonstrates how to:
    * Split the `Route` column (e.g., "BLR → DEL") into separate columns for each stop in the journey.
    * Split the `Dep_Time` column (e.g., "22:20") into `Dep_Hour` and `Dep_Minute` to represent the time numerically.

### 2. Feature Construction
* **Concept**: Feature Construction is the process of creating new features by combining or transforming existing ones. This can help to capture information that isn't explicitly available in the original features.
* **Implementation**: The notebook shows how to:
    * Create a new binary feature named `Business_Class` by checking if the `Additional_Info` column contains the text "Business class".

---
## Key Outcome

By applying these techniques, the original complex and string-based features are transformed into a more structured and numerical format that is easier for machine learning algorithms to process.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**: For data manipulation and feature creation.
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `Train (2).csv` file is in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy jupyter
    ```
4.  Open and run the `feature construction and splitting.ipynb` notebook to see the feature engineering process.
