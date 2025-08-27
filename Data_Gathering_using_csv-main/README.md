# Pandas read_csv() Tutorial and Examples

This repository contains a Jupyter Notebook that serves as a practical guide to using the powerful `pd.read_csv()` function in the pandas library. It covers various parameters and techniques for loading and parsing different types of CSV and other delimited files.

---
## Overview

This notebook is designed as a hands-on tutorial and a cheatsheet for anyone looking to master data ingestion with pandas. It provides clear, executable examples for a wide range of common scenarios you might encounter when working with flat files.

---
## Key Features & Parameters Covered ⚙️

The notebook provides code examples for the following `pd.read_csv()` functionalities:

### 📖 **Basic Reading**
* Loading a standard CSV file from a local directory.
* Reading a CSV file directly from a URL using the `requests` library.

### 📄 **File Formatting & Structuring**
* **`sep`**: Handling different delimiters, such as reading tab-separated files (`.tsv`).
* **`names`**: Providing custom column names when the file lacks a header.
* **`index_col`**: Setting a specific column as the DataFrame's index.
* **`header`**: Specifying which row to use as the column headers.

### 🔧 **Data Selection & Cleaning**
* **`usecols`**: Selecting a subset of columns to load, which can improve memory efficiency.
* **`skiprows`**: Skipping specific rows from the file.
* **`nrows`**: Reading only a specified number of rows from a large file.
* **`na_values`**: Specifying custom strings that should be interpreted as `NaN` (missing values).
* **`on_bad_lines`**: Skipping rows that cause parsing errors.

### 💡 **Type Conversion & Advanced Handling**
* **`dtype`**: Forcing a specific data type for a column upon import.
* **`parse_dates`**: Automatically converting columns with date-like strings to `datetime` objects.
* **`converters`**: Applying a custom function to a column during the reading process.
* **`encoding`**: Reading files with non-standard character encodings (e.g., `'latin-1'`).
* **`chunksize`**: Reading a very large dataset in smaller, manageable chunks to conserve memory.

---
## Technologies Used 💻
* **Python**
* **Pandas**
* **Requests**
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone the repository to your local machine.
2.  Make sure you have the required datasets in the same directory (e.g., `aug_train.csv`, `zomato.csv`, etc.).
3.  Install the necessary libraries:
    ```bash
    pip install pandas requests jupyter
    ```
4.  Open and run the `read_csv.ipynb` notebook to see the examples in action.

````
