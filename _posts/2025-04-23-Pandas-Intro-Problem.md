---
layout: post
title: Pandas Basics Practice Problems Solved
date: 2025-04-23 15:30:0 +0000
categories: [python]
tags: [python, problem, pandas, practice]
---

# Pandas Introduction: Data Loading and Inspection - Practice Exercises

This post provides practice exercises based on the first part of our Pandas learning journey: understanding the basics of the Pandas library, creating DataFrames, loading data from external files, and performing initial data inspection.

Working through these exercises will help solidify your understanding of how to get data into Pandas and take a first look at its structure and content.

---

## Practice Exercises

Use your preferred Python environment (local installation, Google Colab, etc.) to complete these exercises.

1.  **Create a DataFrame from a Dictionary:**
    * Create a Python dictionary with at least two keys (representing columns) and lists of data (representing rows). For example, you could use 'Product' and 'Price'.
    * Use `pandas.DataFrame()` to convert this dictionary into a Pandas DataFrame.
    * Print the resulting DataFrame.

2.  **Create a DataFrame from a List of Lists:**
    * Create a Python list where each inner list represents a row of data (e.g., `[['Apple', 1.0], ['Banana', 0.5]]`).
    * Create a separate list for column names (e.g., `['Item', 'Price']`).
    * Use `pandas.DataFrame()` with both the list of lists and the column names list to create a DataFrame.
    * Print the resulting DataFrame.

3.  **Load Data from a CSV File:**
    * Manually create a simple text file named `sales_data.csv` using a text editor (like Notepad, VS Code, etc.). Include a header row and a few rows of comma-separated data. For example:
        ```csv
        Date,Region,Sales
        2023-01-01,North,150
        2023-01-02,South,200
        2023-01-03,East,120
        ```
    * Save this file in the same directory as your Python script (or note the full path).
    * Use `pandas.read_csv()` to load the data from `sales_data.csv` into a DataFrame.
    * Print the loaded DataFrame.

4.  **Inspect the Loaded DataFrame:**
    * Use the `.head()` method on the DataFrame loaded from `sales_data.csv` to view the first few rows.
    * Use the `.info()` method to see a summary of the DataFrame, including column data types and non-null counts.
    * Use the `.describe()` method to get descriptive statistics for any numeric columns (like 'Sales' in the example).
    * Use the `.shape` attribute to find the number of rows and columns.
    * Print the output of each of these inspection methods.

5.  **(Optional) Load Data from an Excel File:**
    * If you have Microsoft Excel or a compatible program, create a simple spreadsheet (`inventory_data.xlsx`) with a few columns and rows.
    * Save the file.
    * Install the `openpyxl` library if you haven't already (`pip install openpyxl`).
    * Use `pandas.read_excel()` to load the data from the `.xlsx` file into a DataFrame.
    * Apply the inspection methods (`.head()`, `.info()`, `.describe()`, `.shape`) to this Excel-loaded DataFrame as well.

---

Working through these exercises will give you hands-on experience with the fundamental steps of starting with data in Pandas. Good luck!
