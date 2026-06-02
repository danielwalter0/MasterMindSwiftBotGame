# 🧠 SwiftBot Master Mind

> A SwiftBot-powered implementation of the classic Mastermind game featuring camera-based colour recognition, score tracking, game logging, and customizable gameplay.

![Java](https://img.shields.io/badge/Java-17+-orange?style=for-the-badge&logo=java)
![SwiftBot](https://img.shields.io/badge/SwiftBot-Robotics-blue?style=for-the-badge)
![CLI](https://img.shields.io/badge/Interface-CLI-green?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-success?style=for-the-badge)

---

## 📖 About The Project

This project is a software design and implementation of the **Master Mind** game using the **SwiftBot robotic platform**. The game combines traditional Mastermind mechanics with computer vision, allowing players to enter guesses using physical colour cards scanned through the SwiftBot camera.

Players attempt to guess a randomly generated secret colour sequence while receiving feedback after each attempt. The application supports both default and customized game modes, maintains a running scoreboard, and records detailed logs of every game session.

---

## ✨ Features

### 🎮 Gameplay
- Random secret code generation
- Six available colours:
  - 🔴 Red (R)
  - 🟢 Green (G)
  - 🔵 Blue (B)
  - 🟡 Yellow (Y)
  - 🟠 Orange (O)
  - 🩷 Pink (P)
- No duplicate colours in generated codes
- Maximum of 6 attempts in default mode
- Win/Loss detection
- Persistent session scoreboard

### 📷 SwiftBot Camera Integration
- Colour card scanning
- Image processing
- Average RGB calculation
- Automatic colour recognition
- Guess generation from scanned cards

### ⚙️ Custom Game Mode
Players can customise:
- Number of colours in the secret code (3–6)
- Maximum number of attempts

### 📊 Feedback System
After each guess:
- `+` = Correct colour in correct position
- `-` = Correct colour in wrong position

Example:

```text
Secret Code: RGBY
Player Guess: GPBY

Feedback: ++-
```

### 📝 Logging
The system automatically records:
- Round number
- Secret code
- Player guesses
- Remaining attempts
- Scoreboard status
- Date and time

### 🛡 Error Handling
- Invalid colour detection
- Camera recognition failures
- Invalid menu selections
- Invalid custom mode values
- User-friendly error messages

---

## 🏗 System Architecture

```text
┌────────────────────┐
│      Main App      │
└─────────┬──────────┘
          │
          ▼
┌────────────────────┐
│    Game Manager    │
└─────────┬──────────┘
          │
 ┌────────┼─────────┐
 ▼        ▼         ▼

Code    Camera    Logger
Engine  Module    Module

          │
          ▼

    Score Manager
```

---

## 📂 Project Structure

```text
SwiftBot-MasterMind/
│
├── src/
│   ├── Main.java
│   ├── GameManager.java
│   ├── CodeGenerator.java
│   ├── ColourDetector.java
│   ├── FeedbackCalculator.java
│   ├── ScoreManager.java
│   ├── GameLogger.java
│   └── Utilities.java
│
├── logs/
│   └── game_log.txt
│
├── assets/
│   └── colour_cards/
│
├── docs/
│   ├── SRS.pdf
│   ├── Flowcharts.pdf
│   └── UI_Design.pdf
│
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- Java 17 or later
- SwiftBot API
- SwiftBot Robot
- Colour cards (R, G, B, Y, O, P)

### Installation

1. Clone the repository

```bash
git clone https://github.com/yourusername/swiftbot-mastermind.git
```

2. Navigate to the project directory

```bash
cd swiftbot-mastermind
```

3. Compile the project

```bash
javac Main.java
```

4. Run the application

```bash
java Main
```

---

## 🎮 How To Play

### Select a Game Mode

```text
Press A → Default Mode
Press B → Custom Mode
```

### Scan Colour Cards

Follow the prompts:

```text
Scan Colour 1
Scan Colour 2
Scan Colour 3
Scan Colour 4
```

### Receive Feedback

```text
Guess: GPBY
Feedback: ++-
Attempts Left: 3
```

### End of Game

```text
Congratulations! You cracked the code!
```

or

```text
Game Over!
The secret code was RGBY.
```

### Continue or Quit

```text
Press Y to play again
Press X to quit
```

---

## 📈 Additional Features

- Session scoreboard tracking
- Detailed game history logging
- Enhanced user feedback
- Colour recognition validation
- Modular object-oriented design
- Custom difficulty settings

---

## 🧪 Testing

The application has been tested for:

- Secret code generation
- Feedback accuracy
- Colour recognition
- Score calculations
- Logging functionality
- Error handling
- Edge cases

---

## 📚 Academic Context

Developed as part of:

**CS1813 – Software Design**

The project demonstrates:

- Software Requirements Engineering
- Algorithm Design
- User Interface Design
- Object-Oriented Programming
- Software Documentation
- Project Planning & Development

---

## 👨‍💻 Author

**Your Name**

Computer Science Student  
Brunel University London

GitHub: https://github.com/yourusername

---

## 📄 License

This project was developed for educational purposes as part of university coursework.

© 2026 All Rights Reserved.

---

⭐ If you found this project useful, consider starring the repository!
