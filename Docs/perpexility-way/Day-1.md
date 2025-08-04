Here is a detailed, highly structured plan for your first day of a data engineering roadmap, broken down by hour. Each hour includes precise topics, specific tasks, self-assessment questions, a challenge, and a tricky ("stretch") question related to the topic.

## Hour 1: Python Environment Setup & Data Types

**Tasks and Sub-tasks**
- Set up Python (confirm installation, open your IDE).
- Initialize a code project/repo.
- Write and execute a “hello world” program in your IDE and via the command line.
- Explore Python data types:
  - Declare variables of type int, float, str, list, dict, tuple, set, and bool.
  - Print types using `type()`.
  - Convert between types, e.g., int to float, str to int.

**Self-Check Questions**
- What is the difference between a list and a tuple in Python?
- How would you convert the string '42' to the integer 42?

**Challenge**
- Write a script that takes a list containing integers and strings and creates two separate lists: one for all integers, one for all strings.

**Tricky Question**
- How does Python handle mutable vs. immutable types? Why are lists mutable but tuples are not?

## Hour 2: Python Operators & Control Flow

**Tasks and Sub-tasks**
- Practice arithmetic, comparison, and logical operators.
- Write `if`, `elif`, and `else` statements for decision-making.
- Create two short loops:
  - A `for` loop that prints numbers from 1 to 10.
  - A `while` loop that accumulates the sum of numbers until the sum exceeds 50.

**Self-Check Questions**
- What will the following code print?
  ```python
  x = 7
  if x > 10:
      print("big")
  elif x > 5:
      print("medium")
  else:
      print("small")
  ```
- What’s the difference between `==` and `is` in Python?

**Challenge**
- Write a function that takes a number and prints whether it is “positive”, “negative”, or “zero”.

**Tricky Question**
- Consider this code snippet:
  ```python
  a = [1,2,3]
  b = a
  a.append(4)
  print(b)
  ```
  What does it print, and why?

## Hour 3: Working with Lists, Dictionaries, and Loops

**Tasks and Sub-tasks**
- Create a list of numbers and use a loop to print only the even numbers.
- Create a dictionary mapping names to ages, and use a `for` loop to print all names where the age is over 18.
- Practice list comprehensions to square all numbers in a list.

**Self-Check Questions**
- How do you add an element to a list and update a value in a dictionary?
- How would you iterate over key-value pairs in a dictionary?

**Challenge**
- Write a program that takes a dictionary of exam scores and computes the highest score and the corresponding student’s name.

**Tricky Question**
- Can you write a list comprehension that returns all keys from a dictionary whose values are prime numbers? Assume you have a function is_prime().

## Hour 4: File I/O Fundamentals

**Tasks and Sub-tasks**
- Open a text file and print every line.
- Read a small CSV file (you can create it with some sample data).
- Parse the CSV using the `csv` or `pandas` library (if time).
- Split the content into data fields and print only the rows where a numeric field is above a threshold.

**Self-Check Questions**
- What is the difference between reading a file with `read()`, `readline()`, and `readlines()`?
- How do you safely open and close a file in Python?

**Challenge**
- Write a script that reads a CSV file of people (name, age), and writes out another file with only those people older than 21.

**Tricky Question**
- How would you handle the scenario where the CSV file is very large (millions of lines)? List 2 methods to process such a file efficiently without running out of memory.

