# Number Guessing Game🎯

📸 Python Essentials Project

A simple command-line **Number Guessing Game** developed in Python. The player selects a difficulty level, receives a randomly generated number within a specified range, and tries to guess it within a limited number of attempts.

The project demonstrates core Python programming concepts such as conditional statements, loops, functions from the standard library, user input, exception handling, random number generation, arithmetic operations, and basic game logic.

---

🚀 1. Project Overview

The **Number Guessing Game** is an interactive console-based application designed to make basic Python programming concepts practical and easy to demonstrate.

At the beginning of the game, the player chooses one of three difficulty levels:

- **Easy** – Number range: 1 to 50, with 10 attempts
- **Medium** – Number range: 1 to 100, with 7 attempts
- **Hard** – Number range: 1 to 200, with 5 attempts

The computer randomly selects a secret number. The player then enters guesses until the number is found or the available attempts are exhausted.

The game provides feedback after every valid guess, including whether the guess is too high or too low and a distance-based hint.

---

🕹️ 2. Objectives

The main objectives of this project are:

1. To create an interactive Python command-line application.
2. To use Python conditional statements for decision-making.
3. To use loops for repeated user interaction.
4. To generate random numbers using Python's `random` module.
5. To handle invalid user input safely.
6. To implement a difficulty-based scoring system.
7. To provide useful hints based on the difference between the guess and the secret number.
8. To demonstrate how multiple Python concepts can be combined into one working application.

---

🧮 3. Features

### Difficulty Selection

The player can select:

| Difficulty | Number Range | Attempts | Bonus |
|---|---:|---:|---:|
| Easy | 1–50 | 10 | +5 |
| Medium | 1–100 | 7 | +10 |
| Hard | 1–200 | 5 | +20 |

### Random Number Generation

The computer generates a new secret number randomly for every game using Python's `random.randint()` function.

### Guess Validation

The program checks whether the user:

- Entered a valid integer.
- Entered a number within the selected range.

Invalid input does not consume an attempt.

### Guess Feedback

After a valid incorrect guess, the game tells the player:

- **Too low** – the secret number is higher.
- **Too high** – the secret number is lower.

### Distance-Based Hints

The program also calculates the difference between the player's guess and the secret number.

- Difference of 5 or less → **Very close**
- Difference of 6–15 → **Close**
- Difference greater than 15 → **Far away**

### Scoring System

The score depends on the number of attempts remaining when the correct number is guessed.

Basic score:

`Remaining Attempts × 10`

Difficulty bonus:

- Easy: +5
- Medium: +10
- Hard: +20

Therefore, choosing a harder difficulty provides a larger bonus.

### Game Over Handling

If the player uses all attempts without guessing the correct number, the game displays the correct number and a score of 0.

---

## 4. Technologies Used

- **Programming Language:** Python 3
- **Interface:** Command Line / Terminal
- **Library Used:** `random`
- **External Packages:** None

The project uses only Python's standard library, so no additional package installation is required.

---

## 5. Python Concepts Demonstrated

This project demonstrates several important Python Essentials concepts:

### Variables

Variables are used to store:

- Difficulty
- Minimum and maximum range
- Number of attempts
- Secret number
- User guess
- Score
- Difference between numbers

### Conditional Statements

`if`, `elif`, and `else` are used for:

- Difficulty selection
- Input validation
- Comparing guesses
- Selecting hints
- Calculating difficulty bonuses

### While Loop

A `while` loop controls the repeated guessing process while attempts remain.

### For-Else Style Game Completion Logic

The project uses the `while ... else` structure to handle the situation where the loop ends naturally because all attempts have been used.

### Exception Handling

`try` and `except ValueError` prevent the program from crashing when the user enters something that cannot be converted to an integer.

### Random Number Generation

The `random` module is used to generate the secret number.

### Arithmetic Operations

The project uses multiplication, addition, comparison, and absolute difference calculations for scoring and hints.

### String and User Input Handling

The `input()` function is used to receive choices and guesses from the player.

---

## 6. Project Workflow

```text
START
  |
  v
Display Game Title
  |
  v
Display Difficulty Options
  |
  v
Player Selects Difficulty
  |
  +---- Invalid Choice ----> Display Error --> END
  |
  v
Set Range and Attempts
  |
  v
Generate Random Number
  |
  v
Ask Player for Guess
  |
  v
Is Input a Valid Number?
  |
  +---- No ----> Display Error --> Ask Again
  |
  v
Is Guess Within Range?
  |
  +---- No ----> Display Range Error --> Ask Again
  |
  v
Is Guess Correct?
  |
  +---- Yes ----> Calculate Score --> Display Result --> END
  |
  +---- No ----> Display High/Low Feedback
                    |
                    v
              Calculate Hint
                    |
                    v
              Reduce Attempt
                    |
                    v
              Attempts Left?
                    |
             +------+------+
             |             |
            Yes            No
             |             |
             v             v
         Ask Again      Game Over
                           |
                           v
                          END
```

---

## 7. File Structure

The project can be kept simple with the following structure:

```text
Number-Guessing-Game/
│
├── main.py
└── README.md
```

### `main.py`

Contains the complete Python source code for the game.

### `README.md`

Contains project documentation, setup instructions, features, workflow, and technical information.

---

## 8. Requirements

Before running the project, make sure Python 3 is installed.

No external Python libraries are required.

### Recommended Environment

- Python 3.x
- Windows, macOS, or Linux
- Command Prompt, PowerShell, Terminal, or an IDE such as VS Code

---

## 9. How to Run the Project

### Step 1: Install Python

Install Python 3 if it is not already installed.

During installation on Windows, make sure the option to add Python to the system PATH is selected.

### Step 2: Open the Project Folder

Open a terminal or Command Prompt and navigate to the folder containing `main.py`.

Example:

```bash
cd path/to/Number-Guessing-Game
```

### Step 3: Run the Program

Use:

```bash
python main.py
```

If your system uses `python3`, use:

```bash
python3 main.py
```

### Step 4: Select Difficulty

The program displays:

```text
1. Easy
2. Medium
3. Hard
```

Enter `1`, `2`, or `3`.

### Step 5: Enter Guesses

Enter an integer within the displayed range.

The program provides feedback after every incorrect guess.

---

## 10. Example Execution

Example:

```text
======================================
        NUMBER GUESSING GAME
======================================

Choose Difficulty:
1. Easy
2. Medium
3. Hard
Enter your choice (1/2/3): 2

Difficulty: Medium
Guess a number between 1 and 100
You have 7 attempts.

Enter your guess: 40
Too low! Try a higher number.
Hint: You are far away.
Attempts remaining: 6

Enter your guess: 65
Too high! Try a lower number.
Hint: You are close.
Attempts remaining: 5

Enter your guess: 58
Congratulations!
You guessed the correct number.
The correct number was: 58
Your score: 60

======================================
             GAME FINISHED
======================================
```

The exact secret number and score will vary because the number is randomly generated for every game.

---

## 11. Input Validation

The program handles common invalid inputs.

### Invalid Difficulty

If the player enters anything other than `1`, `2`, or `3`, the program displays:

```text
Invalid choice.
```

### Non-Numeric Guess

If the player enters text instead of a number:

```text
Please enter a valid number.
```

The program then asks for another guess.

### Number Outside the Range

If the player enters a number outside the selected range:

```text
Please enter a number within the given range.
```

The attempt is not reduced.

---

## 12. Scoring Logic

The scoring system rewards players for finding the number while they still have attempts remaining.

### Formula

```text
Score = Remaining Attempts × 10 + Difficulty Bonus
```

Difficulty bonuses:

```text
Easy   = +5
Medium = +10
Hard   = +20
```

For example, if a Medium game is won with 5 attempts remaining:

```text
5 × 10 + 10 = 60 points
```

If the player does not guess the number within the available attempts:

```text
Score = 0
```

---

## 13. Advantages of the Project

- Simple and easy to operate.
- Requires no external libraries.
- Demonstrates practical Python programming.
- Provides multiple difficulty levels.
- Includes input validation.
- Gives interactive feedback.
- Uses random number generation.
- Includes a scoring mechanism.
- Can be expanded with additional features in the future.

---

## 14. Possible Future Enhancements

The current version can be extended with features such as:

1. Multiple rounds.
2. High-score tracking.
3. Player name and score history.
4. Replay option without restarting the program.
5. Timer-based scoring.
6. Leaderboard functionality.
7. Difficulty customization.
8. Saving game results to a file.
9. Graphical user interface.
10. Statistics such as average attempts and win rate.

These features are not required for the current version but provide possible directions for future development.

---

## 15. Limitations

The current version is intentionally designed as a lightweight command-line application.

- Scores are not permanently stored.
- There is no graphical interface.
- The game currently runs for one round at a time.
- The secret number is generated randomly and is not saved after the game ends.

---

## 16. Project Conclusion

The Number Guessing Game is a practical Python project that combines several fundamental programming concepts into a single interactive application.

The project demonstrates how variables, conditional statements, loops, exception handling, arithmetic operations, user input, and Python's random number generation can work together to create a complete command-line program.

The application is simple enough to run in a basic Python environment while still demonstrating important programming logic and user interaction.

---

## 17. Author

**Name:** D.Vishnupriya   
**Registration Number:** :26BAI10614   
**Course:** Python Essentials  
**Institution:** VIT Bhopal University

---

## 18. License

This project is created for educational and academic purposes.
