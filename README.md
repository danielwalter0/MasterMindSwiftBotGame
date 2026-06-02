# 🧠 SwiftBot Master Mind

A Java implementation of the classic Master Mind game developed for the SwiftBot platform as part of the CS1813 Software Design module.

![Java](https://img.shields.io/badge/Java-17+-orange?style=for-the-badge&logo=java)
![SwiftBot](https://img.shields.io/badge/SwiftBot-Robotics-blue?style=for-the-badge)
![CLI](https://img.shields.io/badge/Interface-CLI-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

The game combines colour recognition, score tracking, game logging, and a command-line interface to create an interactive code-breaking experience between the player and SwiftBot.

---

## Features

- Random secret code generation
- Six available colours:
  - Red (R)
  - Green (G)
  - Blue (B)
  - Yellow (Y)
  - Orange (O)
  - Pink (P)
- No duplicate colours in generated codes
- Command-line user interface
- Feedback system using:
  - `+` Correct colour and correct position
  - `-` Correct colour but wrong position
- Score tracking
- Game logging
- Input validation and error handling
- Default and Custom game modes

---

## Project Structure

```text
.
├── Colour.java
├── ConsoleUI.java
├── GameController.java
├── GameLogger.java
├── SecretCode.java
├── Main.java
├── Instructions
├── pom.xml
└── README.md
```

### Class Overview

| Class | Responsibility |
|---------|---------------|
| Main | Program entry point |
| GameController | Handles game flow and logic |
| SecretCode | Generates and manages secret codes |
| Colour | Colour definitions and utilities |
| ConsoleUI | User interaction and display |
| GameLogger | Records game information to file |

---

## Gameplay

### Default Mode

- Generates a secret code of 4 colours.
- Colours cannot repeat.
- Player has 6 attempts to guess the code.

### Custom Mode

Players can configure:

- Number of colours (3–6)
- Maximum number of attempts

---

## Example

```text
Secret Code Length: 4

Enter Guess: RGBY

Feedback:
++-

Attempts Remaining: 4
```

### Feedback Rules

| Symbol | Meaning |
|----------|----------|
| + | Correct colour in correct position |
| - | Correct colour in wrong position |

Example:

```text
Code: RGBY
Guess: GPBY

Result: ++-
```

---

## Running the Project

### Clone Repository

```bash
git clone https://github.com/YOUR_USERNAME/swiftbot-mastermind.git
```

### Compile

```bash
mvn clean compile
```

### Run

```bash
mvn exec:java
```

Or run directly from your IDE.

---

## Technologies Used

- Java
- Maven
- Object-Oriented Programming
- File Handling
- Command-Line Interface (CLI)

---

## Learning Outcomes

This project demonstrates:

- Software Requirements Analysis
- Algorithm Design
- Object-Oriented Design
- Error Handling
- File Management
- User Interface Design
- Software Documentation

---

## Author

Developed as part of the **CS1813 Software Design** coursework at Brunel University London.

---

## License

This project is for educational purposes only.
