# Handling Time and Date Data in Pandas

This project provides a comprehensive guide to working with **time and date data** using the pandas library. The Jupyter Notebook demonstrates how to load temporal data, convert it to the proper `datetime` format, and perform various feature engineering tasks to extract valuable information from date and time columns.

---
## Datasets

The notebook uses two sample datasets:
* **`orders.csv`**: Contains a `date` column.
* **`messages.csv`**: Contains a `date` column with both date and time information.

---
## Feature Engineering from Datetime Objects 🕒

The notebook covers the following techniques using the `.dt` accessor in pandas:

### 1. Loading Time Series Data
* Demonstrates using the **`parse_dates`** argument in `pd.read_csv()` to automatically convert date columns to the `datetime64[ns]` data type upon loading.

### 2. Extracting Date Features
* Extracting components from a date column, such as:
    * **Year** (`.dt.year`)
    * **Month** (`.dt.month`) and **Month Name** (`.dt.month_name()`)
    * **Day** (`.dt.day`) and **Day of Week** (`.dt.day_name()`)
    * **Day of Year** (`.dt.dayofyear`)
    * **Week of Year** (`.dt.isocalendar().week`)
* Boolean checks like **`is_month_start`** and **`is_quarter_end`**.

### 3. Extracting Time Features
* Extracting components from a time column, including:
    * **Hour** (`.dt.hour`)
    * **Minute** (`.dt.minute`)
    * **Second** (`.dt.second`)

### 4. Calculating Time Differences (Timedelta)
* Shows how to calculate the duration between two dates to create a `Timedelta` object, which is useful for analyzing time spans.

---
## Technologies Used 💻
* **Python**
* **Pandas** & **NumPy**
* **Jupyter Notebook**

---
## How to Use This Repository

1.  Clone this repository to your local machine.
2.  Ensure the `orders.csv` and `messages.csv` files are in the same directory.
3.  Install the required libraries:
    ```bash
    pip install pandas numpy jupyter
    ```
4.  Open and run the `time and date.ipynb` notebook to see the different time and date manipulation techniques.
