# C++ Chess Engine ♟️

A custom-built chess engine developed entirely in C++. This project focuses on implementing the complete rules of chess, managing board states, and executing complex, multi-layered game logic through robust software architecture.

## Overview
This engine was designed to showcase strong algorithmic thinking and software development capabilities. It heavily utilizes Object-Oriented Programming (OOP) paradigms to manage the diverse behaviors of different chess pieces and the overall state of the game.

## Key Technical Concepts
* **Language:** C++
* **Object-Oriented Programming:** * **Inheritance:** Utilized a base `Piece` class with derived classes for specific pieces (e.g., `Pawn`, `Knight`, `Queen`) to share common attributes while allowing specific movement logic.
  * **Polymorphism:** Implemented virtual functions to dynamically handle piece validation and movement execution at runtime.
* **Algorithmic Logic:** Complex conditional logic to handle special chess rules such as castling, en passant, and pawn promotion, alongside standard move validation.

## How to Run
1. Clone this repository to your local machine.
2. Compile the source files using a standard C++ compiler (e.g., GCC or MSVC).
   ```bash
   g++ main.cpp -o chess_engine
