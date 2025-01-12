# Lesson 5: Functions and Systems of Equations

## Objectives:
- Learn how to create and use functions in Python.
- Solve systems of two equations with two unknowns.
- Practice debugging functions and implementing mathematical logic.

---

### 1. Vocabulary: Functions in Python

| Keyword      | Meaning                                   | Example                     |
|--------------|-------------------------------------------|-----------------------------|
| `def`        | Defines a new function                   | `def my_function():`       |
| `return`     | Sends a value back from a function       | `return x + y`             |
| `parameter`  | Input variable for a function            | `def add(a, b):`           |
| `argument`   | Value passed to a function’s parameter   | `add(2, 3)`                |
| `docstring`  | A description of the function’s purpose  | `"""This adds two numbers"""` |

#### Exercise 1: Match the keyword to its description.
1. Defines a new function → ________
2. Input variable for a function → ________
3. Sends a value back from a function → ________

---

### 2. Writing and Using Functions

#### Basic Function Syntax:
```python
def greet(name):
    """Greets the user by name."""
    return f"Hello, {name}!"

print(greet("Alice"))  # Output: Hello, Alice!
```

#### Example Code:
```python
def add_numbers(a, b):
    """Adds two numbers and returns the result."""
    return a + b

result = add_numbers(5, 7)
print("The sum is:", result)  # Output: The sum is: 12
```

#### Exercise 2: Write the following functions.
1. `subtract_numbers(a, b)`: Subtracts \( b \) from \( a \).
2. `multiply_numbers(a, b)`: Multiplies two numbers.
3. `divide_numbers(a, b)`: Divides \( a \) by \( b \), handling the case where \( b = 0 \).

---

### 3. Solving Systems of Equations

#### System of Two Equations:
A system of equations in two variables:
\[
\begin{aligned}
    a_1x + b_1y &= c_1 \\
    a_2x + b_2y &= c_2
\end{aligned}
\]

#### Steps to Solve:
1. Rearrange one equation to express \( x \) or \( y \) in terms of the other variable.
2. Substitute into the second equation.
3. Solve for one variable, then substitute back to find the other.

#### Example Code:
```python
def solve_system(a1, b1, c1, a2, b2, c2):
    """Solves a system of two equations with two unknowns."""
    determinant = a1 * b2 - a2 * b1
    if determinant == 0:
        return "No unique solution"
    
    x = (c1 * b2 - c2 * b1) / determinant
    y = (a1 * c2 - a2 * c1) / determinant
    return x, y

# Example usage:
solution = solve_system(2, 1, 5, 1, -1, 1)
print("Solution:", solution)  # Output: Solution: (2.0, 1.0)
```

#### Exercise 3: Solve these systems using the function above.
1. \( 3x + 4y = 10 \) and \( 2x - y = 1 \).
2. \( x - 2y = 4 \) and \( 3x + y = 7 \).
3. \( 2x + 3y = 6 \) and \( 4x + 6y = 12 \).

---

### 4. Debugging Functions

#### Common Errors:
1. Forgetting the colon (`:`) at the end of the function definition.
2. Using undefined variables inside the function.
3. Not handling edge cases (e.g., division by zero).

#### Debugging Examples:
1. ```python
    def add_numbers(a, b)
        return a + b
   ```
2. ```python
    def solve_system(a1, b1, c1, a2, b2, c2):
        x = c1 / a1
        return x, y
   ```
3. ```python
    def divide(a, b):
        return a / b  # Fails when b == 0
   ```

#### Exercise 4: Fix the errors in the examples above.

---

### 5. Challenge: Automate Equation Solving

#### Problem:
Write a program that:
1. Prompts the user for the coefficients \( a_1, b_1, c_1, a_2, b_2, c_2 \).
2. Uses a function to solve the system of equations.
3. Displays the solution or a message if there is no unique solution.

#### Example Code:
```python
def main():
    print("Solve a system of equations:")
    a1 = float(input("Enter a1: "))
    b1 = float(input("Enter b1: "))
    c1 = float(input("Enter c1: "))
    a2 = float(input("Enter a2: "))
    b2 = float(input("Enter b2: "))
    c2 = float(input("Enter c2: "))

    solution = solve_system(a1, b1, c1, a2, b2, c2)
    print("Solution:", solution)

main()
```

#### Exercise 5: Extend the program.
1. Add input validation to ensure the user enters numbers.
2. Allow the user to solve multiple systems without restarting the program.

---

### Homework:
1. Write a function to solve a quadratic equation \( ax^2 + bx + c = 0 \) using the discriminant.
2. Create a program that uses functions to evaluate and compare two linear equations (e.g., which grows faster as \( x \) increases).
3. Write a script to determine if three points form a triangle and, if so, calculate its area.

---

By the end of this lesson, you should understand:
- How to define and use functions in Python.
- How to solve systems of equations programmatically.
- How to debug and extend mathematical logic in Python.
