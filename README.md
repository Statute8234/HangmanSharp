# HangmanSharp

The project is a C#-based Hangman game where players guess letters to reveal a hidden word. The game uses a hangman figure as visual feedback, gradually appearing as incorrect guesses are made. The game continues until the player correctly guesses all letters or the figure is drawn, indicating a loss.

## Table of Contents

- [About](#about)
- [Features](#features)
- [Imports](#Imports)
- [Rating: 7/10](#Rating)

# About

The Hangman game is a C# console-based game where players guess letters to reveal a hidden word. The game provides visual feedback in the form of a hangman figure, which gradually appears as incorrect guesses are made. Players must guess all the letters in the word before the hangman figure is fully drawn to win. The program randomly selects a word from a dictionary and displays it as a series of underscores. If a guess is correct, the word is revealed, and if incorrect, the hangman figure is drawn.

# Features

The Hangman game in C# combines word guessing, visual feedback, and suspense to help players solve a hidden word. Players guess letters to reveal a hidden word, with the goal being to identify all the letters in the word. As players make incorrect guesses, a hangman figure gradually appears, representing their progress. The program randomly selects a word from a predefined dictionary, with the chosen word remaining hidden initially. The word is displayed as underscores, representing unknown letters in the word. When a player guesses a correct letter, it is revealed in the word, replacing the underscores with the correctly guessed letters. The game continues until the player guesses the entire word or the hangman is fully drawn.

# Imports

System, System.Collections.Generic, static System.Random, System.Text

# Rating

The code implements a basic hangman game where the player guesses letters to complete a hidden word. It handles user input, tracks guessed letters, displays the hangman figure, and provides feedback. The code is structured into meaningful functions, enhancing readability and maintainability. Variable names are descriptive and follow a consistent naming convention, improving code clarity.
However, the code lacks comprehensive error handling, such as addressing non-alphabetic characters or empty inputs. Adding error handling mechanisms would improve the game's robustness. The UI presentation of the hangman figure and hidden word is visually appealing and easy to understand.
The game logic for checking if a guessed letter is correct or incorrect is implemented correctly, but could be more efficient by using the `Contains` method of the `String` class. The game terminates correctly when the player correctly guesses the word or makes six incorrect guesses, with the message "Game Over" displayed.
Additional comments to explain the purpose of each function or complex logic would improve readability, especially for future maintenance or collaboration. Overall, the code effectively implements the hangman game with good functionality and structure, but with improvements in error handling, efficiency, and comments, it could achieve an even higher rating.
