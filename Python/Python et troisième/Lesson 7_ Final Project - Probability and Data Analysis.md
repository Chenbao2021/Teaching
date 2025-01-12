# Lesson 7: Final Project - Probability and Data Analysis

## Objectives:
- Combine concepts of probability, simulations, and data visualization.
- Develop a comprehensive Python program that integrates various skills.
- Practice debugging, modular programming, and storytelling with data.

---

### 1. Project Overview

You will create a Python project that:
1. Simulates a random experiment (e.g., dice rolls, coin flips, or a game).
2. Calculates probabilities and displays frequency distributions.
3. Visualizes the results using `matplotlib`.

This project should include:
- User input for customization.
- Modular design with functions.
- Clear output and meaningful visualizations.

---

### 2. Step 1: Planning the Project

#### Example Ideas:
1. **Simulating a Lottery:**
   - Draw 6 random numbers from 1 to 49.
   - Calculate the probability of matching all 6 numbers.
2. **Dice-Based Game:**
   - Players roll multiple dice.
   - The player with the highest total wins.
3. **Coin Flip Analysis:**
   - Flip a coin 1000 times.
   - Analyze streaks of "Heads" or "Tails."

#### Exercise 1:
Write a plan for your project:
1. What random experiment will you simulate? → ________
2. What data will you analyze? → ________
3. How will you visualize the results? → ________

---

### 3. Step 2: Writing Modular Code

#### Example Structure:
1. **Input Function:** Collect parameters from the user.
2. **Simulation Function:** Run the random experiment.
3. **Analysis Function:** Calculate probabilities and frequencies.
4. **Visualization Function:** Create plots using `matplotlib`.

#### Example Code:
```python
import random
import matplotlib.pyplot as plt

# Step 1: Input Function
def get_user_input():
    rounds = int(input("Enter the number of simulations: "))
    return rounds

# Step 2: Simulation Function
def simulate_coin_flips(rounds):
    results = [random.choice(["Heads", "Tails"]) for _ in range(rounds)]
    return results

# Step 3: Analysis Function
def analyze_results(results):
    heads = results.count("Heads")
    tails = results.count("Tails")
    return {"Heads": heads, "Tails": tails}

# Step 4: Visualization Function
def visualize_results(frequencies):
    plt.bar(frequencies.keys(), frequencies.values(), color=['blue', 'green'])
    plt.title("Coin Flip Results")
    plt.xlabel("Outcome")
    plt.ylabel("Frequency")
    plt.show()

# Main Program
rounds = get_user_input()
results = simulate_coin_flips(rounds)
frequencies = analyze_results(results)
visualize_results(frequencies)
```

#### Exercise 2:
1. Modify the example to simulate rolling a die instead of flipping a coin.
2. Add a feature to track streaks of consecutive "Heads" or "Tails."

---

### 4. Step 3: Adding Advanced Features

#### Examples of Advanced Features:
1. **Multi-Round Games:**
   - Allow users to play multiple rounds and track cumulative results.
2. **Dynamic Input Validation:**
   - Ensure users provide valid input (e.g., positive integers).
3. **Comparative Visualization:**
   - Plot multiple datasets on the same graph.

#### Example Code:
```python
# Adding Dynamic Input Validation
def get_validated_input(prompt):
    while True:
        try:
            value = int(input(prompt))
            if value > 0:
                return value
            else:
                print("Please enter a positive number.")
        except ValueError:
            print("Invalid input. Please enter a number.")

rounds = get_validated_input("Enter the number of simulations: ")
print(f"You chose to run {rounds} simulations.")
```

#### Exercise 3:
1. Add input validation to your project.
2. Allow users to save results to a file for future reference.

---

### 5. Step 4: Finalizing the Project

#### Checklist for Completion:
1. Does the project have clear input and output?
2. Are functions used to organize the code?
3. Are edge cases handled (e.g., invalid input)?
4. Are the results visualized effectively?

#### Final Challenge:
- Combine all elements into a single cohesive program.
- Add a "Replay" option to let users rerun the simulation with different parameters.

---

### Homework:
1. Write a report summarizing your project:
   - Describe the random experiment.
   - Explain the results and what they mean.
   - Include screenshots of the visualizations.
2. Present your project to the class, explaining the code and your findings.

---

By the end of this lesson, you should be able to:
- Plan and implement a complete Python project.
- Apply probability and data analysis concepts in a real-world context.
- Create modular and reusable code for simulations and visualizations.
