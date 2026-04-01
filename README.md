# DSOOP Chess Engine ♟️

A fully functional, 2D interactive chess game developed in C++ using the **SFML (Simple and Fast Multimedia Library)** for graphics and input handling. This project demonstrates strong Object-Oriented Programming (OOP) principles and implements complex chess rules including castling, en passant, and pawn promotion.

## Features
* **Graphical User Interface:** Modern green/cream checkered board with smooth piece rendering.
* **Interactive Move Indicators:** * Subtle yellow highlighting for selected pieces.
  * Semi-transparent green dots to indicate valid safe moves.
  * Red target rings to indicate valid capture moves (including en passant captures).
* **Complete Chess Logic:**
  * Standard piece movement and collision detection.
  * **Castling:** King and Rook coordinate to move simultaneously.
  * **En Passant:** Complex pawn capture logic implemented and tracked via `Vector2i enPassantTarget`.
  * **Pawn Promotion:** Interactive on-screen menu allowing players to choose between Queen, Rook, Bishop, or Knight.
* **Game State Management:** Automated detection of "Check" and "Checkmate" conditions.

## Tech Stack & Architecture
* **Language:** C++
* **Graphics Library:** SFML (Simple and Fast Multimedia Library)
* **Object-Oriented Design:**
  * **Base Class:** An abstract `Piece` class handles shared properties (textures, position, scaling).
  * **Derived Classes:** `Pawn`, `Rook`, `Knight`, `Bishop`, `Queen`, and `King` classes inherit from `Piece` and override the `isValidMove()` virtual function with their specific movement logic (Polymorphism).
  * **Board Management:** A `Board` class manages the 8x8 grid of pointers, handles texture loading, processes mouse input, and controls the game loop.

## Prerequisites
To compile and run this project, you will need:
* A C++ compiler (GCC, MSVC, or Clang).
* The [SFML Library](https://www.sfml-dev.org/download.php) installed and configured on your system.

### ⚠️ Asset Requirements
This repository contains the engine code, but does not include the graphical assets. Before compiling and running the executable, you must provide 12 standard chess piece PNG images in the same directory as the executable. 

Please ensure the images are named exactly as follows:
* `chess_piece_2_black_pawn.png`
* `chess_piece_2_black_rook.png`
* `chess_piece_2_black_knight.png`
* `chess_piece_2_black_bishop.png`
* `chess_piece_2_black_queen.png`
* `chess_piece_2_black_king.png`
* `chess_piece_2_white_pawn.png`
* `chess_piece_2_white_rook.png`
* `chess_piece_2_white_knight.png`
* `chess_piece_2_white_bishop.png`
* `chess_piece_2_white_queen.png`
* `chess_piece_2_white_king.png`

## Compilation (Example using GCC)
Make sure your SFML include and lib directories are correctly linked.
```bash
g++ main.cpp -o chess_game -lsfml-graphics -lsfml-window -lsfml-system
./chess_game
