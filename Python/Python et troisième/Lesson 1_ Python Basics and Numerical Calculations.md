# Lesson 1: Python Basics and Numerical Calculations

## Objectives:
- Review the order of operations and numerical calculations.
- Learn Python basics: arithmetic operators, `math` library, and functions.
- Practice debugging, writing functions, and solving mathematical problems.

---

### 1. Vocabulary: Python Arithmetic

| Operator | Meaning                       | Example       |
|----------|-------------------------------|---------------|
| `+`      | Addition                      | `2 + 3 = 5`   |
| `-`      | Subtraction                   | `5 - 2 = 3`   |
| `*`      | Multiplication                | `3 * 4 = 12`  |
| `/`      | Division                      | `8 / 2 = 4.0` |
| `**`     | Exponentiation (power)        | `2 ** 3 = 8`  |
| `%`      | Modulus (remainder)           | `10 % 3 = 1`  |

#### Exercise 1: Match the operator to its meaning.
1. `**` → ________
2. `%` → ________
3. `*` → ________

---

### 2. Order of Operations

#### Priority Rules:
1. Parentheses `()`
2. Exponentiation `**`
3. Multiplication `*`, Division `/`, Modulus `%`
4. Addition `+`, Subtraction `-`

#### Example Calculation:
```python
result = (3 + 5) * 2 ** 2 - 4 / 2
print(result)  # Output: 30.0
```

#### Exercise 2: Calculate the result of the following expressions.
1. `(8 + 2) * 3`
2. `10 - 4 ** 2 + 6`
3. `(12 / 4) * (3 + 5)`

#### Exercise 3: Debugging Errors
Find and fix the errors in these Python expressions:
1. `result = 5 + (2 * 3`
2. `value = 4 ** - 3 + 2`
3. `output = 10 / (3 - 3)`

---

### 3. Using the `math` Library

#### Common Functions:
- `math.sqrt(x)`: Square root of `x`.
- `math.pow(x, y)`: \(x^y\).
- `math.factorial(x)`: Factorial of `x`.
- `math.pi`: Constant \(\pi\).

#### Example Code:
```python
import math
radius = 5
area = math.pi * math.pow(radius, 2)
print("Area of the circle:", area)
```

#### Exercise 4: Solve using `math`.
1. Compute the square root of 144.
2. Calculate the area of a circle with radius 7.
3. Find the factorial of 6.

#### Exercise 5: Debugging Errors with `math`
Fix the errors in these codes:
1. `import maths
value = math.sqrt[64]`
2. `result = math.factorial(4.5)`
3. `circle_area = math.pi * radius ** 2  # radius is undefined`

---

### 4. Writing Functions

#### Syntax:
```python
def function_name(parameters):
    # Code block
    return value
```

#### Example Function:
```python
def calculate_circle_area(radius):
    import math
    return math.pi * math.pow(radius, 2)

area = calculate_circle_area(5)
print("Circle Area:", area)
```

#### Exercise 6: Write the following functions.
1. `solve_expression(a, b, c)`:
   - Input: three numbers.
   - Output: result of \(a^2 + b^2 - c\).
2. `is_divisible(x, y)`:
   - Input: two numbers.
   - Output: True if `x` is divisible by `y`, else False.
3. `calculate_hypotenuse(a, b)`:
   - Input: two sides of a right triangle.
   - Output: the hypotenuse.

#### Exercise 7: Debugging Functions
Fix the errors in these functions:
1. ````python
    def add_numbers(a, b)
        return a + b
    ````
2. ```python
    def calculate_square_area(side):
        return side * side
    result = calculate_square_area()
    ```
3. ```python
    def invalid_function(x):
        print("Result:" x)
    ```

---

### 5. Challenge: Combine Concepts

#### Problem:
Write a Python program to solve this problem:
- Input: A radius \(r\).
- Output: The area and circumference of a circle, calculated using functions.

#### Example Code:
```python
def calculate_area(radius):
    import math
    return math.pi * math.pow(radius, 2)

def calculate_circumference(radius):
    import math
    return 2 * math.pi * radius

radius = float(input("Enter the radius: "))
print("Area:", calculate_area(radius))
print("Circumference:", calculate_circumference(radius))
```

#### Exercise 8: Modify the program.
1. Add input validation to ensure the radius is positive.
2. Allow the user to repeat the calculation for multiple radii.

---

### Homework:
1. Write a function to solve this equation: \((a + b)^2 - c^2\).
2. Create a program that asks for the side lengths of a rectangle and outputs its area and perimeter.
3. Write a Python script to find the largest number among three inputs using a function.

---

By the end of this lesson, you should understand:
- How to use Python operators and the `math` library.
- The importance of debugging and finding errors.
- How to write and use functions to solve mathematical problems.
