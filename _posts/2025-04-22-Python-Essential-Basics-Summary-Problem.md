---
layout: post
title: Python Essential Basics Practice Problems Solved
date: 2025-04-22 12:50:0 +0000
categories: [python]
tags: [python, problem, basics, practice]
---

# Python Essential Basics Practice Problems - Solved

Practicing fundamental Python concepts is crucial for building a strong programming foundation, especially before diving into libraries like Pandas for data analysis. I've worked through a set of basic Python practice problems, covering variables, data types, operators, data structures (lists, tuples, dictionaries, sets), control flow (if, for, while), and functions.

Below are the problems and my solutions, displayed directly for easy viewing.

---

## 1. Variables, Data Types, and Basic Operators Practice

**Problem:**

You purchased 3 books from an online bookstore.  
The price of the first book is 15 USD (`book1_price`), the second is 20 USD (`book2_price`), and the third is 12 USD (`book3_price`).  
Calculate the total purchase amount (`total_price`), and the final price (`final_price`) after a 10% discount.  
Print both.

**Hint:** Use `int`, `float`, `+`, `*`, `-`.

**Solution:**

```python
# Define individual book prices
book1_price = 15
book2_price = 20
book3_price = 12

# Define discount rate
discount_rate = 0.1  # 10% discount

# Calculate total price before discount
total_price = book1_price + book2_price + book3_price

# Calculate final price after applying discount
final_price = total_price * (1 - discount_rate)

# Print results
print("Total Price:", total_price)
print("Final Price after discount:", final_price)

2. List Practice
Problem:

Create a list called weekly_fruits that contains at least 5 different fruits you want to eat this week.

Print the first and last fruits from the list.

Add 'mango' to the end of the list.

Change the second fruit in the list to 'kiwi'.

Check if 'apple' is in the list and print the result.

Hint: Use [], indexing, append(), in, list reassignment.

Solution:

# Create a list of fruits
weekly_fruits = ["apple", "banana", "pear", "grape", "pineapple"]

# Print the first and last fruit
print(weekly_fruits[0], weekly_fruits[-1])  # First and last items using index

# Add 'mango' to the list
weekly_fruits.append("mango")

# Replace the second fruit with 'kiwi'
weekly_fruits[1] = "kiwi"

# Print the updated list
print(weekly_fruits)

# Check if 'apple' is in the list
print('apple' in weekly_fruits)  # Returns True or False

3. Tuple Practice
Problem:

Store the latitude and longitude of a city in a tuple called city_location in the format (latitude, longitude).

Assign the first element (latitude) and the second element (longitude) of the tuple to separate variables and print them.

Hint: Use tuple creation (), indexing [], or unpacking a, b = tuple_var.

Solution:

# Create a tuple to store latitude and longitude
city_location = (37.5665, 126.9780)  # Example: Seoul

# Unpack the tuple into two variables
latitude, longitude = city_location

# Print each variable
print("Latitude:", latitude)
print("Longitude:", longitude)

4. Dictionary Practice
Problem:

Create a dictionary called study_group where each key is a member's name and the value is another dictionary with their age and role.

Change the role of 'Charlie' to 'Treasurer'.

Add a new member 'Sarah' with role 'Member' and age 31.

Print the role of 'Daniel'.

Check whether 'Emily' exists in the dictionary and print the result.

Hint: Use {}, key-based access and update, adding new key-value pairs, in operator.

Solution:

# Create dictionary of study group members
study_group = {
    'Charlie': {'age': 25, 'role': 'Member'},
    'John': {'age': 24, 'role': 'Leader'},
    'Daniel': {'age': 26, 'role': 'Treasurer'}
}

# Update Charlie's role to 'Treasurer'
study_group['Charlie']['role'] = 'Treasurer'

# Add a new member, Sarah'
study_group['Sarah'] = {'age': 31, 'role': 'Member'}

# Print Daniel's role
print(study_group['Daniel']['role'])

# Check if 'Emily' is in the group
print('Emily' in study_group)  # Returns True or False

5. Set Practice
Problem:

You have a list with some duplicate subjects: ['CS', 'Math', 'Physics', 'CS', 'Chemistry', 'Math']

Create a set unique_subjects that only contains unique subjects.

Add 'Biology' to the set.

Remove 'Math' from the set.

Print the set and check if 'Physics' is in the set.

Hint: Use set(), .add(), .remove(), in.

Solution:

# Original list with duplicates
all_subjects_list = ['CS', 'Math', 'Physics', 'CS', 'Chemistry', 'Math']

# Create a set to keep only unique subjects
unique_subjects = set(all_subjects_list)

# Add 'Biology' to the set
unique_subjects.add('Biology')

# Remove 'Math' from the set
unique_subjects.remove('Math')  # Use discard() if you're not sure it exists

# Print the updated set
print(unique_subjects)

# Check if 'Physics' is in the set
print('Physics' in unique_subjects)  # Returns True or False

6. Conditional Statements Practice
Problem:

Store an arbitrary temperature (e.g., 18 degrees Celsius) in a variable called temperature.

Then use conditional statements to print:

"The weather is hot." if temperature is 25 or higher

"The weather is nice." if it's between 15 and 24 (inclusive of 15, exclusive of 25)

"The weather is cool." if it's between 10 and 14 (inclusive of 10, exclusive of 15)

Otherwise, print "The weather is cold."

Hint: Use if, elif, else, comparison operators.

Solution:

# Define a temperature value
temperature = 18

# Use conditional statements to determine weather description
if temperature >= 25:
    print("The weather is hot.")
elif 15 <= temperature < 25:
    print("The weather is nice.")
elif 10 <= temperature < 15:
    print("The weather is cool.")
else:
    print("The weather is cold.")

7. For Loop Practice
Problem:

You have a list of numbers: numbers = [10, 5, 8, 12, 3]

Use a for loop to print each number in the list.

Then, using the range() function, write code that prints only the odd numbers from 1 to 20.

Hint: Use for ... in ..., range(), modulo operator % with if.

Solution:

# List of numbers
numbers = [10, 5, 8, 12, 3]

# Print each number in the list using a for loop
for num in numbers:
    print(num)

# Print odd numbers from 1 to 20 using range() and % operator
for i in range(1, 21):
    if i % 2 != 0:  # Check if the number is odd
        print(i)

8. While Loop Practice
Problem:

Initialize a variable i to 1.

Write a while loop that prints the value of i and increments it by 1 until i is greater than 10.

Then, write another while loop that repeatedly prompts the user for input until they type 'exit'.

Hint: Use while loop, += operator, input() function.

Solution:

# Part 1: Print numbers from 1 to 10 using a while loop
i = 1
while i <= 10:
    print(i)
    i += 1  # Increase i by 1 each time

# Part 2: Keep prompting the user until they type 'exit'
while True:
    user_input = input("Enter 'exit' to finish: ")
    if user_input.strip().lower() == 'exit':  # Normalize input
        break  # Exit the loop if user types 'exit'

print("Loop finished because 'exit' was entered.")

9. Functions Practice
Problem:

Write a function called calculate_circle_area that takes a radius as an argument and returns the area of a circle.

Use the formula: radius * radius * 3.14.

Call the function with a radius of 5, store the result in a variable, and print it.

Write another function called print_list_items that takes a list as an argument and prints each item in the list, one item per line.

Call this function using a list of your favorite colors.

Hint: Use def, parameters, return, function call, loop inside the function.

Solution:

# Function to calculate the area of a circle
def calculate_circle_area(r):
    return r * r * 3.14  # Use π ≈ 3.14

# Call the function with radius 5 and print the result
area = calculate_circle_area(5)
print("Area of Radius 5 is:", area)


# Function to print each item in a list
def print_list_items(items):
    for item in items:
        print(item)  # Print each item on a new line

# Create a list of favorite colors
fav_list = ['yellow', 'orange', 'red']

# Call the function with the color list
print_list_items(fav_list)
