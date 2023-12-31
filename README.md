## Tic Tac Toe Game

This is a simple implementation of the classic game Tic Tac Toe in Python.

### Functions

#### `sum(a, b, c)`

This function takes three parameters, `a`, `b`, and `c`, and returns their sum.

#### `printBoard(xState, zState)`

This function prints the Tic Tac Toe board based on the X and O states passed as parameters. It displays the current state of the board with X and O markings.
Certainly! Let's explain the `printBoard` function in detail.

### `printBoard(xState, zState)`

This function takes two parameters: `xState` and `zState`. These parameters represent the current state of the Tic Tac Toe board for the X and O players, respectively.

The function's purpose is to print the current state of the Tic Tac Toe board, with 'X' for X-player positions and 'O' for O-player positions. If a position is empty, it displays the corresponding position number.

#### Parameters

- `xState`: A list representing the state of the board for X-player.
- `zState`: A list representing the state of the board for O-player.

#### Functionality

The function goes through each position on the board (0 to 8) and checks whether it's taken by X, O, or empty. It then prints the corresponding character or position number.

```python
def printBoard(xState, zState):
    # Checking the state of each position and assigning 'X', 'O', or position number accordingly
    zero = 'X' if xState[0] else ('O' if zState[0] else 0)
    one = 'X' if xState[1] else ('O' if zState[1] else 1)
    # ... (repeat for positions 2 to 8)
    
    # Printing the board with the current state
    print(f"{zero} | {one} | {two}")
    print("--|---|---")
    print(f"{three} | {four} | {five}")
    print("--|---|---")
    print(f"{six} | {seven} | {eight}")
```

### Example Usage

```python
xState = [1, 0, 0, 0, 0, 1, 0, 0, 0]  # Example X-player state
zState = [0, 0, 0, 0, 0, 0, 1, 0, 0]  # Example O-player state

# Printing the board with the current state
printBoard(xState, zState)
```

Output:
```
X | 1 | 2
--|---|---
3 | 4 | O
--|---|---
6 | 7 | 8
```

In this output, the positions taken by X and O are displayed, and empty positions are represented by their corresponding position numbers.

#### `checkWin(xState, zState)`

This function checks if there is a winner in the Tic Tac Toe game based on the current X and O states. It checks for all possible winning combinations and declares the winner accordingly.
Sure, let's break down the `checkwin` function step by step.

### `checkwin(xState, zState)`

This function checks if there is a winner in the Tic Tac Toe game based on the current X and O states. It evaluates if any player (X or O) has a winning combination of positions on the board.

#### Parameters

- `xState`: A list representing the state of the board for X-player.
- `zState`: A list representing the state of the board for O-player.

#### Functionality

1. **`wins`**: This is a list of lists, each sub-list representing a winning combination of positions on the Tic Tac Toe board. For example, `[0, 1, 2]` represents the top row positions, and `[0, 3, 6]` represents the left column.

2. **Loop through Winning Combinations**:
   It iterates through each winning combination (each sub-list in `wins`).

   ```python
   for win in wins:
   ```

3. **Check X-player's Win**:
   It sums up the values in X-player's positions for the current win combination and checks if the sum is 3 (which means all three positions in that combination are occupied by X). If so, it prints that X wins the match and returns `1` to indicate X's victory.

   ```python
   if sum(xState[win[0]], xState[win[1]], xState[win[2]]) == 3:
       print("X wins the match")
       return 1
   ```

4. **Check O-player's Win**:
   It does the same for O-player, checking if the sum of positions in the current win combination is 3. If so, it prints that O wins the match and returns `0` to indicate O's victory.

   ```python
   if sum(zState[win[0]], zState[win[1]], zState[win[2]]) == 3:
       print("O wins the match")
       return 0
   ```

5. **No Winner Found**:
   If no winner is found after checking all the winning combinations, it returns `-1` to indicate that the game is still ongoing.

   ```python
   return -1
   ```

### Main Execution

The `if __name__ == "__main__":` block is the main execution of the program. It initializes the X and O states, sets the starting player (X), and runs the game loop until there is a winner or a draw. In each iteration, it alternates between X and O players, takes input for their moves, updates the game state, and checks for a winner. If a winner is found, it prints the winner and ends the game.

### How to Run

To run the Tic Tac Toe game, execute the Python script. The program will prompt you to enter a value indicating your move (0-8) on the Tic Tac Toe board. The game will display the board, take your input, and continue until there is a winner or a draw.

Certainly! Let's provide an overview of the Tic Tac Toe game.

## Tic Tac Toe Game Overview

Tic Tac Toe, also known as noughts and crosses, is a classic two-player game typically played on a 3x3 grid. The players take turns marking a square with their symbol (usually 'X' for the first player and 'O' for the second). The goal is to be the first to get three of their symbols in a row, either horizontally, vertically, or diagonally.

### Objective

The main objective of Tic Tac Toe is to create a continuous line of three of your symbols (either 'X' or 'O') in a row, column, or diagonal on the game grid.

### Rules

1. **Grid**: The game is played on a 3x3 grid, but variations with larger grids are also possible.

2. **Players**: Two players participate, usually denoted as 'X' and 'O'. 'X' goes first.

3. **Moves**: Players take turns to place their symbol in an empty cell on the grid.

4. **Winning**: A player wins by placing three of their symbols in a horizontal, vertical, or diagonal row.

5. **Draw**: If all cells are filled and no player has three in a row, the game is a draw.

### Gameplay

1. **Start**: The game starts with an empty grid.

2. **Player Turns**: Players take turns to place their symbol in an empty cell.

3. **Winning**: The game continues until one player achieves three in a row or all cells are filled (resulting in a draw).

4. **Win Announcement**: If a player wins, the game announces the winner. If it's a draw, the game announces a draw.

### Strategy

- Players often start in the center cell to maximize potential winning moves.
- Blocking the opponent's winning moves is crucial to prevent them from winning.
- Corners are valuable positions since they can be part of multiple winning combinations.

Tic Tac Toe is a simple yet engaging game, often used as a learning tool for basic strategy and logical thinking, particularly for children. It's a staple of childhood games and is widely known and played around the world.

