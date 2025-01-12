# Lesson 3: Loops and Sequences

## Objectives:
- Learn how to use `for` and `while` loops in Python.
- Understand and implement arithmetic and geometric sequences.
- Practice debugging loops and writing functions to work with sequences.

---

### 1. Vocabulary: Loops in Python

| Keyword      | Meaning                             | Example                                   |
|--------------|-------------------------------------|-------------------------------------------|
| `for`        | Loop that iterates over a sequence  | `for i in range(5):`                     |
| `while`      | Loop that continues while a condition is true | `while x < 10:`               |
| `range()`    | Function that generates a sequence of numbers | `range(1, 10, 2)`               |
| `break`      | Exit the loop early                | `if x > 5: break`                        |
| `continue`   | Skip the current iteration         | `if x == 3: continue`                    |

#### Exercise 1: Match the keyword to its description.
1. A loop that runs while a condition is true → ________
2. Exits a loop early → ________
3. Generates a sequence of numbers → ________

---

### 2. Using `for` Loops

#### Steps to Use:
1. Use `range()` to generate a sequence of numbers.
2. Iterate through the sequence with a `for` loop.

#### Example Code:
```python
for i in range(1, 6):
    print("Number:", i)
```

#### Exercise 2: Write the output for these examples.
1. `for i in range(3): print(i)` → ________
2. `for i in range(2, 10, 2): print(i)` → ________
3. `for i in range(5, 0, -1): print(i)` → ________

#### Exercise 3: Debugging `for` Loops
Fix the errors in these examples:
1. ```python
    for i in range(5)
        print(i)
    ```
2. ```python
    for i in 1, 2, 3:
        print(i)
    ```
3. ```python
    for i in range(3):
    print("Loop:", i)
    ```

---

### 3. Using `while` Loops

#### Steps to Use:
1. Define a condition for the loop.
2. Ensure the condition changes within the loop to avoid infinite loops.

#### Example Code:
```python
x = 1
while x <= 5:
    print("Value:", x)
    x += 1
```

#### Exercise 4: Write the output for these examples.
1. ```python
    x = 0
    while x < 3:
        print(x)
        x += 1
    ```
2. ```python
    x = 10
    while x > 5:
        print(x)
        x -= 2
    ```
3. ```python
    x = 1
    while x < 10:
        if x == 5:
            break
        print(x)
        x += 1
    ```

#### Exercise 5: Debugging `while` Loops
Fix the errors in these examples:
1. ```python
    x = 0
    while x < 5
        print(x)
        x += 1
    ```
2. ```python
    x = 0
    while x < 3:
    print(x)
        x += 1
    ```
3. ```python
    x = 1
    while x < 10:
        if x == 7:
            continue
        print(x)
        x += 1
    ```

---

### 4. Arithmetic and Geometric Sequences

#### Arithmetic Sequence:
- Formula: \( u_n = u_1 + (n - 1) \cdot r \)
- `u_1`: First term, `r`: Common difference, `n`: Term number.

#### Example Code:
```python
def arithmetic_sequence(u1, r, n):
    terms = []
    for i in range(n):
        terms.append(u1 + i * r)
    return terms

print(arithmetic_sequence(2, 3, 5))  # Output: [2, 5, 8, 11, 14]
```

#### Geometric Sequence:
- Formula: \( u_n = u_1 \cdot r^{n-1} \)
- `u_1`: First term, `r`: Common ratio, `n`: Term number.

#### Example Code:
```python
def geometric_sequence(u1, r, n):
    terms = []
    for i in range(n):
        terms.append(u1 * (r ** i))
    return terms

print(geometric_sequence(3, 2, 4))  # Output: [3, 6, 12, 24]
```

#### Exercise 6: Write functions for sequences.
1. `arithmetic_sum(u1, r, n)`: Calculate the sum of the first \( n \) terms of an arithmetic sequence.
2. `geometric_sum(u1, r, n)`: Calculate the sum of the first \( n \) terms of a geometric sequence.
3. `nth_term_arithmetic(u1, r, n)`: Return the \( n \)-th term of an arithmetic sequence.

---

### 5. Challenge: Generate and Analyze Sequences

#### Problem:
Write a program that:
1. Prompts the user to choose arithmetic or geometric sequences.
2. Asks for `u1`, `r`, and `n`.
3. Generates the sequence and calculates its sum.

#### Example Code:
```python
def main():
    choice = input("Choose sequence type (arithmetic/geometric): ").strip().lower()
    u1 = int(input("Enter the first term (u1): "))
    r = int(input("Enter the common difference/ratio (r): "))
    n = int(input("Enter the number of terms (n): "))

    if choice == "arithmetic":
        sequence = arithmetic_sequence(u1, r, n)
        total = sum(sequence)
    elif choice == "geometric":
        sequence = geometric_sequence(u1, r, n)
        total = sum(sequence)
    else:
        print("Invalid choice.")
        return

    print("Sequence:", sequence)
    print("Sum:", total)

main()
```

#### Exercise 7: Extend the program.
1. Add input validation for `n` (must be a positive integer).
2. Allow the user to calculate only specific terms (e.g., the 5th term).

---

### Homework:
1. Write a function to generate the first \( n \) odd numbers using a loop.
2. Create a program to calculate the factorial of a number using a `while` loop.
3. Write a script that uses loops to draw a multiplication table (from 1 to 10).

---

By the end of this lesson, you should understand:
- How to use `for` and `while` loops effectively in Python.
- How to work with arithmetic and geometric sequences.
- How to debug and extend loops in practical applications.
