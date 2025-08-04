# Daily Plan: Monday, August 4, 2025 (Week 1, Day 1 – Python Programming Basics)

**Objective**: Master Python variables, data types, basic functions, error handling, and pandas basics for data manipulation, setting the foundation for data engineering tasks.

**Total Time**: 4 hours (9:00 AM – 1:00 PM)

## Hour 1: Python Variables and Data Types (9:00 AM – 10:00 AM)
**Topics**: Variables, data types (int, float, string, list, dictionary), basic operations, type conversion.

### Sub-Tasks
1. **Learn Variables and Data Types (20 minutes)**:
   - Watch a 15-minute video on Python variables and data types (e.g., freeCodeCamp’s “Python for Beginners” on YouTube, first 15 minutes).
   - Take notes on how to declare variables (e.g., `x = 10`, `name = "Alice"`) and understand types (int, float, str, list, dict).
2. **Practice Variable Operations (25 minutes)**:
   - Create variables: `price = 19.99`, `items = [1, 2, 3]`, `customer = {"id": 101, "name": "John"}`.
   - Perform operations: Calculate `total_price = price * len(items)` and print it.
   - Convert types: Change `price` to int (`int(price)`) and print the result.
3. **Explore Lists and Dictionaries (15 minutes)**:
   - Add an item to `items` using `items.append(4)`.
   - Add a new key-value pair to `customer` (e.g., `customer["email"] = "john@example.com"`).
   - Print all dictionary values using a loop.

### Questions to Test Understanding
1. What is the difference between `int` and `float` data types in Python?
2. How do you add an element to a list and access a dictionary value by key?
3. What happens if you try to convert the string `"abc"` to an integer using `int("abc")`?

### Expected Answers
1. `int` represents whole numbers (e.g., 5), while `float` represents decimals (e.g., 5.0).
2. Use `list.append(item)` to add to a list; access dictionary values with `dict[key]`.
3. It raises a `ValueError` because `"abc"` cannot be converted to an integer.

## Hour 2: Functions and Error Handling (10:00 AM – 11:00 AM)
**Topics**: Defining functions, parameters, return statements, try/except for error handling.

### Sub-Tasks
1. **Learn Functions (20 minutes)**:
   - Read “Automate the Boring Stuff with Python” (Chapter 3, Functions, ~10 pages, free online).
   - Understand function syntax: `def function_name(parameters): return value`.
2. **Write a Function (25 minutes)**:
   - Create a function `calculate_total(prices)` that takes a list of prices and returns their sum.
   - Test it with `prices = [10.5, 20.0, 15.75]` and print the result.
3. **Add Error Handling (15 minutes)**:
   - Modify the function to handle non-numeric inputs using try/except.
   - Example: `try: return sum(prices) except TypeError: return "Invalid input"`.

### Questions to Test Understanding
1. What does the `return` statement do in a function?
2. How does `try/except` help in handling errors?
3. What error would occur if you pass an empty list to `sum()` in a function?

### Expected Answers
1. `return` sends a value back from a function and ends its execution.
2. `try/except` catches errors (e.g., TypeError) to prevent crashes and allows custom error handling.
3. Passing an empty list to `sum()` returns 0, as `sum([])` is defined to return 0.

## Hour 3: Introduction to Pandas (11:00 AM – 12:00 PM)
**Topics**: Reading CSVs, basic DataFrame operations, saving results.

### Sub-Tasks
1. **Learn Pandas Basics (20 minutes)**:
   - Watch a 15-minute pandas tutorial (e.g., “Pandas in 10 Minutes” on YouTube).
   - Understand `pd.read_csv()`, DataFrame filtering, and `to_csv()`.
2. **Process a CSV (25 minutes)**:
   - Download a sample CSV (e.g., create a file `sales.csv` with columns: `order_id, product, price, quantity` or use a Kaggle dataset like “Retail Sales”).
   - Write a script to:
     - Read the CSV into a DataFrame (`df = pd.read_csv("sales.csv")`).
     - Calculate total sales (`df["total"] = df["price"] * df["quantity"]`).
     - Save results to `sales_summary.csv`.
3. **Filter Data (15 minutes)**:
   - Filter rows where `quantity > 1` using `df[df["quantity"] > 1]`.
   - Print the filtered DataFrame.

### Questions to Test Understanding
1. How do you read a CSV file into a pandas DataFrame?
2. What does `df["column_name"]` do in pandas?
3. How can you save a DataFrame to a CSV file?

### Expected Answers
1. Use `pd.read_csv("filename.csv")` to read a CSV into a DataFrame.
2. `df["column_name"]` accesses a specific column in the DataFrame as a Series.
3. Use `df.to_csv("filename.csv", index=False)` to save a DataFrame to a CSV.

## Hour 4: Challenge and Review (12:00 PM – 1:00 PM)
**Topics**: Apply all concepts in a mini-project, debug, and commit to Git.

### Sub-Tasks
1. **Mini-Project: Sales Data Processor (30 minutes)**:
   - Combine today’s skills in a script:
     - Read `sales.csv` into a pandas DataFrame.
     - Write a function `process_sales(df)` that:
       - Filters rows with `price > 10`.
       - Calculates total sales per product using groupby (`df.groupby("product")["total"].sum()`).
       - Handles errors (e.g., missing columns).
     - Save results to `product_sales.csv`.
2. **Debug and Comment (15 minutes)**:
   - Test your script with a malformed CSV (e.g., missing `price` column).
   - Add comments to explain each step in your code.
3. **Git Setup (15 minutes)**:
   - Initialize a Git repository (`git init`).
   - Commit your scripts (`git add .`, `git commit -m "Day 1: Python and pandas basics"`).

### Challenge
- **Task**: Modify `process_sales(df)` to handle a CSV where `price` is stored as a string with a dollar sign (e.g., `"$19.99"`). Convert it to float and calculate total sales.
- **Steps**:
  - Use `df["price"] = df["price"].str.replace("$", "").astype(float)`.
  - Test with a sample CSV containing prices like `"$10.50"`.
- **Expected Output**: A DataFrame with correct total sales, saved to `product_sales.csv`.

### Tricky Questions
1. What happens if you try to access a non-existent key in a dictionary (e.g., `customer["age"]`)? How can you avoid an error?
2. In pandas, what’s the difference between `df.loc[]` and `df.iloc[]`? Why might you use one over the other?
3. If your function receives a list with mixed types (e.g., `[1, "2", 3.5]`), how would you ensure `calculate_total` sums only numbers?

### Expected Answers
1. Accessing a non-existent key raises a `KeyError`. Avoid it using `dict.get("key", default)` (e.g., `customer.get("age", 0)`).
2. `df.loc[]` uses label-based indexing (e.g., column names), while `df.iloc[]` uses integer-based indexing. Use `loc` for column names, `iloc` for row/column positions.
3. Use a list comprehension or filter: `sum(x for x in lst if isinstance(x, (int, float)))` to sum only numeric values.

## Notes
- **Setup**: Install Python 3.9+ and pandas (`pip install pandas`). Use VS Code for coding.
- **Sample CSV**: Create `sales.csv` with:
  ```
  order_id,product,price,quantity
  1,Shirt,19.99,2
  2,Pants,29.99,1
  3,Shirt,19.99,3
  ```
- **Breaks**: Take a 5-minute break between hours.
- **Debugging Tips**:
  - Use `print()` to inspect variables.
  - Check pandas errors (e.g., `KeyError` for missing columns).
- **Resources**:
  - Free: “Automate the Boring Stuff with Python” (Chapter 3), pandas documentation, GitHub Desktop tutorial.
  - Optional: Codecademy Python (free tier), Kaggle datasets.