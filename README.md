# Tetris Game in C++

## Introduction
This is a simple console-based Tetris game implemented in C++ using basic concepts of game development. The game features standard Tetris mechanics, including tetromino movement, rotation, line clearing, and score tracking. The game is played within a console window and utilizes Windows-specific functions for smooth rendering.

## Table of Contents
- Installation
- Usage
- Objective
- Functions Used
- Features
- Contributing
- License

## Installation Guide
### 1. Install a C++ Compiler
This game is written in C++, so you'll need a C++ compiler installed to run it.

#### Windows:
- Install MinGW or use Visual Studio, which comes with its own compiler.
- If using MinGW, add it to your system's PATH so you can use the `g++` command from anywhere in the terminal.

#### Mac:
- Install Xcode via the App Store, which includes `clang` (the Mac compiler for C++).

#### Linux:
- Install the build-essential package using this command:
  ```sh
  sudo apt update && sudo apt install build-essential
  ```

### 2. Open the Project in Your IDE
Once you have the files and compiler, open the project in your favorite C++ IDE (such as Visual Studio, Code::Blocks, or CLion). Alternatively, you can use any text editor (like Notepad++, Sublime Text, or VS Code) and compile the code manually.

### 3. Compile the Code
To compile the project, run the following command in your terminal or command prompt:
```sh
g++ tetris.cpp -o tetris_game
```
This will create an executable file called `tetris_game` that you can run.

### 4. Run the Game
Once compiled, you can run the game using:

#### Windows:
```sh
./tetris_game.exe
```

#### Linux/Mac:
```sh
./tetris_game
```

## Play the Game
After running the game, you should see the game board in your terminal. Use the below keys to control the tetromino:

- **A/D** - Move left/right.
- **S** - Move the tetromino down faster.
- **Space** - Hard drop the tetromino.
- **Up Arrow or R** - Rotate the tetromino.
- **Q** - Quit the game.
- **Score increases** by clearing lines.
- The **game ends** when new tetrominoes can no longer fit on the board.

## Prerequisites
- A C++ compiler (MinGW, MSVC, etc.)
- Windows OS (due to `windows.h` and `conio.h` dependencies)

## Steps
1. Clone or download the source code.
2. Open the `.cpp` file in a C++ IDE or text editor.
3. Compile the program using a C++ compiler.
4. Run the compiled executable.

## Usage
Once the game is running, you can start playing:

### Controls:
- **A / D** - Move left/right
- **S** - Move down
- **Space** - Hard drop
- **Up Arrow / R** - Rotate
- **Q** - Quit the game

### Gameplay:
- Tetrominoes fall from the top of the screen.
- Arrange them to form complete horizontal lines, which will disappear and increase your score.
- The game continues until the board is full and no more tetrominoes can be placed.

### Scoring:
- Each cleared line gives **100 points**.
- The game saves your high score in a file (`highscore.txt`) and updates it if you beat your previous record.

### Game Over:
- The game ends when tetrominoes reach the top of the board.
- Your final score is displayed, and you can restart the game by running the program again.

## Objective
- The goal is to clear lines by arranging tetrominoes effectively.
- Avoid filling up the board to keep playing.
- Try to beat your high score!

## Functions Used
- **void loadHighScore()** - Loads the highest score from a file.
- **void saveHighScore()** - Saves the highest score to a file.
- **void drawBoard(const Tetromino& tetromino)** - Draws the current state of the board and the falling tetromino.
- **bool checkCollision(const Tetromino& tetromino)** - Checks if the tetromino collides with the existing blocks or walls.
- **void mergeTetromino(const Tetromino& tetromino)** - Merges the current tetromino into the board after it lands.
- **void clearLines()** - Clears complete lines and updates the score.
- **void rotateTetromino(Tetromino& tetromino)** - Rotates the tetromino if the new position is valid.
- **void gameCountdown()** - Displays a countdown before the game starts.
- **int main()** - Controls the game loop, handling user input, tetromino movement, and rendering.

## Features
- Classic Tetris mechanics
- Seven different tetromino shapes
- Real-time user controls
- Automatic falling pieces
- Line clearing and score tracking
- High score persistence using file I/O
- Console-based rendering with minimal flickering

## Contributing
We welcome contributions from the community! To contribute to the project, follow these steps:

### 1. Fork the Repository
Start by forking the repository to your own GitHub account.

### 2. Clone the Repository
Clone the forked repository to your local machine:
```sh
git clone https://github.com/yourusername/tetris_game.git
```

### 3. Create a New Branch
Create a new branch for your feature or bug fix:
```sh
git checkout -b feature-branch-name
```

### 4. Make Your Changes
Implement your changes or improvements. Ensure your code follows the existing style and structure.

### 5. Test Your Changes
Run the game locally to ensure your changes work as expected and do not introduce new bugs.

### 6. Commit Your Changes
Commit your changes with a clear and descriptive commit message:
```sh
git commit -m "Added feature X to improve game functionality"
```

### 7. Push Your Changes
Push your changes to your forked repository:
```sh
git push origin feature-branch-name
```

### 8. Create a Pull Request
Create a pull request and describe the changes you made.

## License
This project is open-source and free to use under the **MIT License**.

