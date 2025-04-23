---
layout: post
title: Pandas Basics
date: 2025-04-23 15:00:0 +0000
categories: [python]
tags: [python, problem, basics, pandas, DataFrame]
---

# Python Compressed Learning: Week 1 - Pandas Basics

This document outlines the first week of a compressed Python learning plan, focusing on essential Python basics and the fundamentals of the Pandas library for data processing. This is crucial preparation for data-related tasks.

**Overall Goal for Week 1 (April 21st - April 27th):**

Quickly review essential Python syntax and grasp the core concepts of the Pandas library, including understanding DataFrames, loading data from files, and performing basic data inspection.

**Detailed Steps for Week 1:**

1.  **Rapid Review of Essential Python Basics:**
    * Variables and Data Types (Numbers, Strings, Booleans, None)
    * Data Structures (Lists, Tuples, Dictionaries, Sets) - Focus on List and Dictionary usage.
    * Control Flow (if, for, while) - Basic structure and usage.
    * Functions (Definition and Calling) - Simple usage.
    * *(This was covered in previous practice problems.)*

2.  **Pandas Introduction and DataFrame Basics:**
    * Understand what Pandas is and its role in data analysis.
    * Grasp the concepts of Pandas' core data structures (Series, DataFrame).
    * **Create DataFrames directly** from Python dictionaries or lists.
    * **Load data into DataFrames from external files** like CSV and Excel (`pd.read_csv()`, `pd.read_excel()`).
    * Use basic methods to **quickly inspect the content and structure** of a loaded DataFrame:
        * `.head()`: View the first few rows.
        * `.info()`: Get column information, data types, and non-null counts.
        * `.describe()`: See descriptive statistics for numeric columns.
        * `.shape`: Check the number of rows and columns.

---

## Pandas Introduction: Data Loading and Inspection

This section covers the fundamental steps of getting data into a Pandas DataFrame and taking a first look at its contents and structure.

### What is Pandas and Why Use It?

Pandas is a powerful open-source library built on top of Python, designed specifically for data manipulation and analysis. It's the standard tool in Python for working with tabular or structured data.

* **Efficient Data Handling:** Provides fast and flexible data structures for working with large datasets.
* **Rich Functionality:** Offers a wide range of functions for common data tasks like cleaning, filtering, transforming, grouping, and aggregating data.
* **Integration:** Works seamlessly with other popular Python libraries for data science (NumPy, Matplotlib, Seaborn, scikit-learn).

The two primary data structures in Pandas are **Series** (1D labeled array) and **DataFrame** (2D labeled table). We will focus mainly on the **DataFrame**.

### Creating a DataFrame

You can create DataFrames directly from Python's built-in data structures.

* **From a Python Dictionary:** Keys become column names, and values (lists/arrays) become column data.

    ```python
    import pandas as pd # Import the pandas library, commonly aliased as 'pd'

    # Prepare data as a dictionary
    data = {
        'Name': ['Alice', 'Bob', 'Charlie'],
        'Age': [25, 30, 35]
    }

    # Create a DataFrame from the dictionary
    df_from_dict = pd.DataFrame(data)

    # Print the resulting DataFrame
    print("DataFrame from Dictionary:")
    print(df_from_dict)
    ```

* **From a List of Lists:** Each inner list is a row. Column names can be provided separately.

    ```python
    import pandas as pd

    # Prepare data as a list of lists
    data_list = [
        ['Alice', 25],
        ['Bob', 30],
        ['Charlie', 35]
    ]
    column_names = ['Name', 'Age'] # Define column names

    # Create a DataFrame from the list of lists, specifying column names
    df_from_list = pd.DataFrame(data_list, columns=column_names)

    # Print the resulting DataFrame
    print("\nDataFrame from List of Lists:")
    print(df_from_list)
    ```

### Loading Data from External Files

Real-world data typically comes from files. Pandas provides easy functions to read various formats.

* **Reading CSV Files:**

    ```python
    import pandas as pd

    # Assume a CSV file named 'sample_data.csv' exists.
    # Example content of sample_data.csv:
    # ID,Product,Price,Quantity
    # 1,Laptop,1200,5
    # 2,Mouse,25,10
    # 3,Keyboard,75,8
    # 4,Monitor,300,3

    # Use pd.read_csv() to load the data
    # Ensure the file path is correct for your environment
    try:
        df_csv = pd.read_csv('sample_data.csv')
        print("\nDataFrame from CSV File:")
        print(df_csv)
    except FileNotFoundError:
        print("\nError: 'sample_data.csv' not found. Check the file path or create the file.")
    ```
    *(To practice, manually create this file with a text editor.)*

* **Reading Excel (xlsx) Files:**

    ```python
    import pandas as pd

    # May require 'openpyxl' library: pip install openpyxl
    # Assume an Excel file named 'sample_data.xlsx' exists.

    try:
        df_excel = pd.read_excel('sample_data.xlsx')
        print("\nDataFrame from Excel File:")
        print(df_excel)
    except FileNotFoundError:
         print("\nError: 'sample_data.xlsx' not found. Check the file path or upload the file.")
    except ImportError:
         print("\nError: 'openpyxl' library not installed. Install it using 'pip install openpyxl'.")
    ```
    *(To practice, obtain or create a simple `.xlsx` file.)*

### Inspecting a Loaded DataFrame

After loading data, use these methods for a quick overview.

* `df.head(n=5)`: Shows the **first N rows** (default 5).
* `df.info()`: Prints a concise summary: column names, non-null counts, data types, memory usage.
* `df.describe()`: Generates **descriptive statistics** for **numeric columns**.
* `df.shape`: Returns `(number of rows, number of columns)`.

**Example Code (Inspection Methods):**

```python
import pandas as pd

# Example DataFrame (assume loaded from a file)
data = {
    'Name': ['Alice', 'Bob', 'Charlie', 'David', 'Eve', 'Frank'],
    'Age': [25, 30, 35, 40, 28, 32],
    'City': ['Seoul', 'Busan', 'Seoul', 'Jeju', 'Busan', 'Seoul'],
    'Score': [85.5, 90.2, None, 78.0, 92.1, 88.7] # Example with a missing value
}
df = pd.DataFrame(data)

print("--- df.head() (First 5 Rows) ---")
print(df.head())

print("\n--- df.head(3) (First 3 Rows) ---")
print(df.head(3))

print("\n--- df.info() ---")
df.info()

print("\n--- df.describe() (Numeric Column Statistics) ---")
print(df.describe())

print("\n--- df.shape (Rows, Columns) ---")
print(df.shape)
```
