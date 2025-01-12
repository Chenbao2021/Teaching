# Lesson 4: Lists and Representations in Python

## Objectives:
- Understand how to create and manipulate lists in Python.
- Use lists to represent mathematical data (e.g., points on a graph).
- Visualize data using Python’s `matplotlib` library.

---

### 1. Vocabulary: Lists in Python

| Keyword      | Meaning                                   | Example                     |
|--------------|-------------------------------------------|-----------------------------|
| `list`       | A collection of items in a specific order | `my_list = [1, 2, 3]`      |
| `append()`   | Adds an item to the end of a list          | `my_list.append(4)`         |
| `len()`      | Returns the number of items in a list      | `len(my_list)`              |
| `remove()`   | Removes a specific item from the list      | `my_list.remove(2)`         |
| `index()`    | Returns the index of the first occurrence  | `my_list.index(3)`          |

#### Exercise 1: Match the keyword to its description.
1. Adds an item to the end of a list → ________
2. Counts the number of items in a list → ________
3. Returns the position of a specific item → ________

---

### 2. Creating and Manipulating Lists

#### Creating a List:
```python
numbers = [2, 4, 6, 8]
print(numbers)
```

#### Adding Items:
```python
numbers.append(10)
print(numbers)  # Output: [2, 4, 6, 8, 10]
```

#### Removing Items:
```python
numbers.remove(4)
print(numbers)  # Output: [2, 6, 8, 10]
```

#### Example Code:
```python
def add_to_list(lst, item):
    lst.append(item)
    return lst

my_list = [1, 2, 3]
print(add_to_list(my_list, 4))
```

#### Exercise 2: Predict the output.
1. ```python
   nums = [1, 2, 3]
   nums.append(5)
   print(nums)
   ```
   → ________
2. ```python
   nums = [10, 20, 30]
   nums.remove(20)
   print(nums)
   ```
   → ________
3. ```python
   nums = [7, 8, 9]
   print(len(nums))
   ```
   → ________

---

### 3. Representing Mathematical Data with Lists

#### Example: Points on a Graph
```python
x_points = [1, 2, 3, 4]
y_points = [2, 4, 6, 8]
for i in range(len(x_points)):
    print(f"Point: ({x_points[i]}, {y_points[i]})")
```

#### Exercise 3:
1. Write a program to generate points for the line \( y = 2x + 1 \) for \( x \) in range(1, 6).
2. Create lists of \( x \) and \( y \) values for the function \( y = x^2 \), and print them.

---

### 4. Visualizing Data with `matplotlib`

#### Steps to Visualize:
1. Install matplotlib (if needed): `pip install matplotlib`.
2. Import the library: `import matplotlib.pyplot as plt`.
3. Plot the data using `plt.plot()`.

#### Example Code:
```python
import matplotlib.pyplot as plt

x = [1, 2, 3, 4]
y = [1, 4, 9, 16]

plt.plot(x, y, marker='o')
plt.title("Graph of y = x^2")
plt.xlabel("x")
plt.ylabel("y")
plt.grid()
plt.show()
```

#### Exercise 4:
1. Plot the line \( y = 3x + 2 \) for \( x \) in range(0, 10).
2. Visualize the points of the function \( y = -x^2 + 4x + 1 \).
3. Add labels, a title, and a grid to your plots.

---

### 5. Challenge: Combining Lists and Visualization

#### Problem:
Write a program that:
1. Generates \( x \) values from 1 to 10.
2. Computes \( y = 2x + 3 \) and stores the results in a list.
3. Plots the graph of \( y \) vs. \( x \).

#### Example Code:
```python
import matplotlib.pyplot as plt

def generate_points():
    x = list(range(1, 11))
    y = [2 * i + 3 for i in x]
    return x, y

x_vals, y_vals = generate_points()
plt.plot(x_vals, y_vals, marker='o')
plt.title("Graph of y = 2x + 3")
plt.xlabel("x")
plt.ylabel("y")
plt.grid()
plt.show()
```

#### Exercise 5:
1. Modify the program to plot multiple functions on the same graph (e.g., \( y = 2x + 3 \) and \( y = x^2 \)).
2. Use different colors and markers for each function.

---

### Homework:
1. Create a program to compute and plot the first \( n \) terms of an arithmetic sequence.
2. Write a script that generates and visualizes the values of \( y = x^3 - 2x^2 + x \).
3. Create a bar chart to represent the frequencies of numbers in a list (e.g., [1, 2, 2, 3, 3, 3, 4]).

---

By the end of this lesson, you should understand:
- How to create and manipulate lists in Python.
- How to use lists to represent mathematical data.
- How to visualize data using `matplotlib` for better analysis and understanding.
