# 🎯 Guess The Number Game

A simple **Number Guessing Game** built using **Java Swing**. The game generates a random number between **1 and 100**, and the player gets a maximum of **7 attempts** to guess it correctly.

The application also keeps track of game statistics such as total rounds, wins, and average guesses.

## ✨ Features

- 🎲 Generates a random number between **1 and 100**
- 🔢 Maximum of **7 attempts** per round
- ⬆️ Gives a **"Too High!"** hint for incorrect high guesses
- ⬇️ Gives a **"Too Low!"** hint for incorrect low guesses
- ✅ Displays a success message when the number is guessed correctly
- ❌ Reveals the correct number when all attempts are used
- 🔄 **Play Again** functionality for starting a new round
- 📊 Tracks:
  - Total rounds
  - Total wins
  - Average number of guesses
- ⚠️ Validates input and handles invalid/non-integer input
- 🖥️ Desktop GUI built with Java Swing

## 🛠️ Technologies Used

- **Java**
- **Java Swing**
- **AWT**
- **Event Handling**
- **Object-Oriented Programming**

## 🎮 How the Game Works

1. When the application starts, it generates a random number from **1 to 100**.
2. Enter your guess in the input field.
3. Click **Submit**.
4. The game provides feedback:
   - `Too Low!` → your guess is smaller than the target number.
   - `Too High!` → your guess is larger than the target number.
   - `Correct Guess!` → you found the target number.
5. You have **7 attempts** to guess the number.
6. If you win, the number of attempts used is displayed.
7. If all 7 attempts are exhausted, the correct number is revealed.
8. Click **Play Again** to start another round.

## 📊 Statistics

After each completed round, the application updates the statistics displayed at the bottom of the window:

```text
Rounds: 0 | Wins: 0 | Avg Guesses: 0
```

The average is calculated using the total number of guesses divided by the number of completed rounds.

## 🖥️ User Interface

The application uses a dark-themed Swing interface containing:

- Game title
- Guess input field
- Submit button
- Play Again button
- Game message/history area
- Attempts remaining indicator
- Game statistics

## 📁 Project Structure

```text
Guess-The-Number-Game/
│
├── NumberGameSwing.java
└── README.md
```

## ⚙️ Requirements

To run this project, you need:

- **Java Development Kit (JDK)**
- Java compiler (`javac`)
- Java runtime (`java`)

No external libraries or dependencies are required.

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Navigate to the Project Directory

```bash
cd Guess-The-Number-Game
```

### 3. Compile the Java File

```bash
javac NumberGameSwing.java
```

### 4. Run the Application

```bash
java NumberGameSwing
```

A graphical window for the Number Guessing Game will open.

## 🧠 Implementation Details

The main class is `NumberGameSwing`, which extends `JFrame` and implements `ActionListener`.

The game uses:

- `Math.random()` to generate the target number.
- `JTextField` for user input.
- `JTextArea` to display game messages.
- `JLabel` to display attempts and statistics.
- `JButton` for submitting guesses and starting a new game.
- `ActionListener` to handle button interactions.
- `JOptionPane` to display input validation messages.

The target number is generated using:

```java
randomNumber = (int)(Math.random() * 100) + 1;
```

The maximum number of attempts is defined as:

```java
private final int MAX_ATTEMPTS = 7;
```

## 🔢 Game Logic

For every valid guess:

```text
Guess < Target → Too Low
Guess > Target → Too High
Guess = Target → Correct
```

After every incorrect guess, the remaining attempts are calculated as:

```java
int remaining = MAX_ATTEMPTS - guesses;
```

When a round finishes, the game updates the number of rounds, wins, and total guesses.

## 📈 Statistics Calculation

The average number of guesses is calculated as:

```java
double avg = (double) totalGuesses / rounds;
```

The displayed value is formatted to two decimal places.

## 🔮 Possible Future Improvements

Some possible enhancements for future versions:

- Add difficulty levels such as **Easy, Medium, and Hard**
- Add a scoring system
- Add a timer
- Add sound effects
- Add a leaderboard
- Store high scores using a database
- Add customizable number ranges
- Improve the visual design with custom icons and themes
- Add keyboard support for submitting guesses
- Track the best score across multiple sessions

## 👨‍💻 Author

**Yogya Srivastava**

Feel free to modify and extend the project to add new features and improve the user experience.

## 📄 License

This project is intended for educational and personal project purposes.
