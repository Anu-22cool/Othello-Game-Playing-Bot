# Othello Bot Competition

Welcome to the Othello Bot Competition! In this project, you'll code a bot to play and win the game of Othello. The bot will be provided with a board configuration and a turn, and it must return a valid move. The game ends when neither player can make a valid move, and the player with the maximum number of coins wins.

## System Specifications

- **Programming Language**: C++
- **Operating System**: 64-bit Linux distribution

## Getting Started

### Framework Setup

1. Extract the contents of `Desdemona.tar.gz` into a suitable directory.
2. Set up the framework by running the `make` command in the root directory.

### Coding the Bot

- Modify `MyBot.cpp` to return a valid move whenever the function `play` is called. The source file is located at `bots/MyBot`.
- Do not modify any other source files.
- Use the provided makefile at `bots/MyBot` to generate a `.so` file.
- Test your bot against another bot using the command:
    bin/Desdemona <path to bot1.so> <path to bot2.so>
- By convention, the first bot is BLACK and the second is RED.
- A random bot (`bots/RandomBot`) has been provided for testing.
- At the end of the game, a `game.log` file is created that contains the sequence of moves made.
- The bots being submitted must have NO print statements.
- If a bot returns an invalid move, it will be disqualified.
# Othello Game Helper Functions

This repository contains helper functions for implementing an Othello game. These functions facilitate validating moves, making moves, retrieving valid moves, and retrieving counts of black and red coins on the board. 

## functions included:

- **bool validateMove( Turn turn, int x, int y )**
  - Returns true if the move (x,y) is valid for the specified turn; otherwise, returns false.

- **bool validateMove( Turn turn, Move move )**
  - Returns true if the specified move is valid for the specified turn; otherwise, returns false.

- **void makeMove( Turn turn, int x, int y )**
  - Updates the board configuration by making the move (x,y) for the specified turn. Throws an exception if the move is not valid.

- **void makeMove( Turn turn, Move move )**
  - Updates the board configuration by making the specified move for the specified turn. Throws an exception if the move is not valid.

- **list<Move> getValidMoves( Turn turn )**
  - Returns a list of valid moves that can be made given the specified turn.

- **int getBlackCount()**
  - Returns the number of black coins (denoted by 'X') on the board.

- **int getRedCount()**
  - Returns the number of red coins (denoted by 'O') on the board.

- **void print( Turn turn )**
  - Prints the current board configuration with the number of black and red coins. 'X' represents black coins, 'O' represents red coins, and unfilled locations are blank.

## usage:

These functions are designed to be used in conjunction with an Othello board implementation. They provide essential operations for validating moves, updating the board state, and retrieving game statistics.

## time constraints:

Each function is optimized to execute within strict time constraints to ensure smooth gameplay. For instance, operations like validating moves and retrieving valid moves are designed to operate efficiently within a maximum time limit of 2 seconds per move.
