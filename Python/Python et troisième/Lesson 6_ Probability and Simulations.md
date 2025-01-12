
# Lesson 6: Probability and Simulations

## Objectives:
- Understand basic probability concepts and apply them in Python.
- Use Python to simulate random experiments (e.g., dice rolls, coin flips).
- Practice creating and analyzing frequency distributions.

---

### 1. Vocabulary: Probability and Randomness

| Keyword      | Meaning                                   | Example                     |
|--------------|-------------------------------------------|-----------------------------|
| `random`     | Python library for generating random numbers | `import random`            |
| `randint()`  | Generates a random integer in a range     | `random.randint(1, 6)`     |
| `choice()`   | Selects a random item from a list         | `random.choice(['H', 'T'])` |
| `uniform()`  | Generates a random float in a range       | `random.uniform(0, 1)`     |
| `seed()`     | Initializes the random number generator   | `random.seed(42)`          |

#### Exercise 1: Match the keyword to its description.
1. Generates a random integer → ________
2. Selects a random item from a list → ________
3. Initializes the random number generator → ________

---

### 2. Simulating Random Experiments

#### Example: Simulating a Coin Flip
```python
import random

def flip_coin():
    return random.choice(["Heads", "Tails"])

# Simulate 10 coin flips
for _ in range(10):
    print(flip_coin())
```

#### Example: Rolling a Six-Sided Die
```python
def roll_die():
    return random.randint(1, 6)

# Simulate 5 dice rolls
for _ in range(5):
    print(roll_die())
```

#### Exercise 2: Simulate these experiments.
1. Flip a coin 50 times and count the occurrences of "Heads" and "Tails."
2. Roll a six-sided die 100 times and calculate the frequency of each number.

---

### 3. Probability Distributions

#### Example: Simulating and Analyzing Frequencies
```python
import random

# Simulate rolling a die 1000 times
def roll_dice_simulation():
    results = [random.randint(1, 6) for _ in range(1000)]
    frequencies = {i: results.count(i) for i in range(1, 7)}
    return frequencies

print(roll_dice_simulation())
```

#### Exercise 3: Create a Frequency Distribution
1. Write a program to simulate 1000 coin flips and calculate the probability of "Heads."
2. Simulate rolling two dice and calculate the probabilities for the sum of their values.

---

### 4. Visualizing Simulations with Matplotlib

#### Example: Bar Chart of Dice Frequencies
```python
import matplotlib.pyplot as plt
import random

# Simulate rolling a die 1000 times
results = [random.randint(1, 6) for _ in range(1000)]
frequencies = {i: results.count(i) for i in range(1, 7)}

# Prepare data for plotting
sides = list(frequencies.keys())
counts = list(frequencies.values())

# Create bar chart
plt.bar(sides, counts, color='blue')
plt.xlabel("Die Face")
plt.ylabel("Frequency")
plt.title("Die Roll Frequencies (1000 Rolls)")
plt.show()
```

#### Exercise 4: Visualize Results
1. Create a bar chart to display the results of 1000 coin flips.
2. Visualize the probabilities for the sum of two dice rolls (e.g., 2 to 12).

---

### 5. Challenge: Simulate a Game

#### Problem:
Create a program that simulates a simple game:
1. Two players each roll a six-sided die.
2. The player with the higher roll wins.
3. Simulate 1000 rounds and calculate the winning percentage for each player.

#### Example Code:
```python
import random

def roll_dice():
    return random.randint(1, 6)

def simulate_game(rounds):
    player1_wins = 0
    player2_wins = 0

    for _ in range(rounds):
        player1 = roll_dice()
        player2 = roll_dice()
        if player1 > player2:
            player1_wins += 1
        elif player2 > player1:
            player2_wins += 1

    total = player1_wins + player2_wins
    print(f"Player 1 Win Percentage: {player1_wins / total * 100:.2f}%")
    print(f"Player 2 Win Percentage: {player2_wins / total * 100:.2f}%")

simulate_game(1000)
```

#### Exercise 5: Extend the Program
1. Add a rule where ties result in a re-roll.
2. Track and display the average roll for each player over all rounds.

---

### Homework:
1. Simulate and visualize the results of rolling three dice and calculating their sum.
2. Write a program to simulate a lottery where 6 random numbers are drawn from 1 to 49.
3. Create a simulation to estimate the probability of getting at least one "6" in 10 rolls of a die.

---

By the end of this lesson, you should understand:
- How to simulate random experiments in Python.
- How to calculate and visualize probabilities and frequencies.
- How to create and analyze simple games using probability.
