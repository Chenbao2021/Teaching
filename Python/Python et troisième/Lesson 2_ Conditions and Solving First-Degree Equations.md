# Lesson 2: Conditions and Solving First-Degree Equations

## Objectives:
- Understand and use Python conditions (`if`, `elif`, `else`).
- Solve first-degree equations \( ax + b = 0 \) using Python.
- Practice debugging conditional logic and writing equations as functions.

---

### 1. Vocabulary: Conditions in Python

| Keyword   | Meaning                              | Example                                   |
|-----------|--------------------------------------|-------------------------------------------|
| `if`      | Start a condition                    | `if x > 0:`                              |
| `elif`    | Add another condition to check       | `elif x == 0:`                           |
| `else`    | Execute if no other condition is met | `else:`                                  |
| `True`    | A boolean value representing truth   | `if True:`                               |
| `False`   | A boolean value representing falsehood | `if False:`                            |

#### Exercise 1: Match the keyword to its description.
1. Executes only if all other conditions are `False` → ________
2. Adds an additional condition → ________
3. A boolean value that represents truth → ________

---

### 2. Solving Equations \( ax + b = 0 \)

#### Steps to Solve:
1. Rearrange the equation: \( x = -b / a \).
2. Handle edge cases (e.g., \( a = 0 \)).
3. Use conditions to manage these cases.

#### Example Code:
```python
def solve_equation(a, b):
    if a == 0:
        if b == 0:
            return "Infinite solutions"
        else:
            return "No solution"
    else:
        return -b / a

# Example usage:
print(solve_equation(2, -4))  # Output: 2.0
```

#### Exercise 2: Write the output for these examples.
1. `solve_equation(0, 0)` → ________
2. `solve_equation(0, 3)` → ________
3. `solve_equation(5, -10)` → ________

---

### 3. Debugging Conditions

#### Common Errors:
1. Missing colons (`:`) after `if`, `elif`, or `else`.
2. Using `=` instead of `==` for comparison.
3. Incorrect indentation.

#### Debugging Examples:
1. ```python
   def check_positive(x):
       if x > 0
           return "Positive"
       else
           return "Not positive"
   ```
2. ```python
   number = 10
   if number = 10:
       print("Ten")
   ```
3. ```python
   value = -5
   if value > 0:
   print("Positive")
   else:
       print("Negative")
   ```

#### Exercise 3: Fix the errors in the examples above.

---

### 4. Writing Functions for Equations

#### Example: Solve Equations
```python
def solve_linear(a, b, c):
    """Solves equations of the form ax + b = c."""
    if a == 0:
        return "No solution or infinite solutions"
    else:
        return (c - b) / a

print(solve_linear(2, 3, 7))  # Output: 2.0
```

#### Exercise 4: Write these functions.
1. `is_positive(x)`: Returns `True` if \( x > 0 \), else `False`.
2. `find_root(a, b, c)`: Solves \( ax + b = c \).
3. `check_even(x)`: Returns `True` if \( x \) is even, else `False`.

#### Exercise 5: Debugging Functions
Fix the errors in these functions:
1. ```python
    def is_positive(x):
    if x > 0:
        return True
    else
        return False
    ```
2. ```python
    def find_root(a, b):
        return -b / a
    print(find_root(0, 5))
    ```
3. ```python
    def check_even(x):
        if x % 2 == 0
            print("Even")
    ```

---

### 5. Challenge: Implement a Mini Calculator

#### Problem:
Create a program that can solve:
1. \( ax + b = c \)
2. Check if a number is even or odd.
3. Determine if a number is positive, negative, or zero.

#### Example Code:
```python
def mini_calculator():
    print("1. Solve ax + b = c")
    print("2. Check if a number is even or odd")
    print("3. Check if a number is positive or negative")

    choice = int(input("Enter your choice: "))

    if choice == 1:
        a = float(input("Enter a: "))
        b = float(input("Enter b: "))
        c = float(input("Enter c: "))
        print("Solution:", (c - b) / a if a != 0 else "No solution")
    elif choice == 2:
        x = int(input("Enter a number: "))
        print("Even" if x % 2 == 0 else "Odd")
    elif choice == 3:
        x = float(input("Enter a number: "))
        if x > 0:
            print("Positive")
        elif x < 0:
            print("Negative")
        else:
            print("Zero")
    else:
        print("Invalid choice")

mini_calculator()
```

#### Exercise 6: Extend the program.
1. Add an option to calculate the absolute value of a number.
2. Add input validation to ensure users enter valid numbers.

---

### Homework:
1. Write a function to check if a number is divisible by another.
2. Create a program to solve \( ax^2 + bx + c = 0 \) using the discriminant.
3. Write a script to determine the larger of two numbers entered by the user.

---

By the end of this lesson, you should understand:
- How to use conditions effectively in Python.
- How to solve first-degree equations programmatically.
- How to debug and extend conditional logic in Python.
