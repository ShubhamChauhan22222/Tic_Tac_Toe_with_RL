# Tic Tac Toe with Reinforcement Learning Agent

## Overview

This repository contains an implementation of a Tic Tac Toe game and a reinforcement learning agent that learns to play the game through Q-learning. The project demonstrates how an AI agent can be trained to make strategic decisions in a simple game environment and provides tools for interactive gameplay and statistical analysis of the agent's performance.

## Table of Contents
- [Usage](#usage)
- [TicTacToeGame Class](#tictactoegame-class)
- [Agent Class](#agent-class)
- [Demo Game Stats Function](#demo-game-stats-function)
- [Main Execution Block](#main-execution-block)
- [Functionality Overview](#functionality-overview)
- [Customization](#customization)

## Usage

1. **Copy the Code:**
   - Copy the entire code in ttt.py file into a Jupyter Notebook or directly run the ttt.py Python script.

2. **Run the Script:**
   - Run the script to train the agent and interactively play Tic Tac Toe.

3. **Interactive Gameplay:**
   - After training, you can play Tic Tac Toe against the agent by following the prompts.
     
4. **Training Notebook:**
   - tic-tac-toe-with-reinforced-learning.ipynb
   - Use this jupyter Notebook for understanding the code and training part.

## TicTacToeGame Class

### Initialization
- **Description:** Initializes a Tic Tac Toe game with an empty board, sets the starting player as 'X', and initializes the 'winner' as `None`.

### Allowed Moves
- **Description:** Returns a list of all possible board states after the current player makes a move.

### Make Move
- **Description:** Updates the game state to the next state provided it's a valid move.

### Playable
- **Description:** Checks if the game is still ongoing (i.e., no winner yet and there are allowed moves).

### Predict Winner
- **Description:** Determines if there is a winner based on the current board state.

### Print Board
- **Description:** Prints the current state of the board in a formatted manner.

## Agent Class

### Initialization
- **Description:** Initializes the reinforcement learning agent with parameters like `epsilon` (exploration rate), `alpha` (learning rate), and the player it will optimize for (`value_player`).

### State Value
- **Description:** Returns the estimated value (Q-value) of a given game state.

### Learn Game
- **Description:** Trains the agent by playing multiple episodes of Tic Tac Toe.

### Learn From Episode
- **Description:** Plays a single episode of Tic Tac Toe and learns from it.

### Learn From Move
- **Description:** Updates the Q-value of the current state based on the reward received and the predicted future rewards.

### Learn Select Move
- **Description:** Selects the next move based on the current policy (exploration vs. exploitation).

### Play Select Move
- **Description:** Selects the next move during gameplay based on the learned Q-values.

### Demo Game
- **Description:** Plays a complete game of Tic Tac Toe either silently or with verbose output.

### Interactive Game
- **Description:** Allows the user to interactively play Tic Tac Toe against the trained agent.

### Round V
- **Description:** Rounds all Q-values to one decimal place.

### Save V Table
- **Description:** Saves the learned Q-values to a CSV file.

### Private Helper Methods
- `__state_values`: Calculates Q-values for all possible moves.
- `__argmax_V`, `__argmin_V`, `__random_V`: Helper methods for selecting moves based on Q-values.
- `__reward`: Computes the reward for the agent based on the game outcome.
- `__request_human_move`: Prompts the user for a valid move during interactive gameplay.

## Demo Game Stats Function

### Demo Game Stats
- **Description:** Runs multiple Tic Tac Toe games to gather statistics on win/draw percentages for 'X', 'O', and draws.

## Main Execution Block

- **Initialization:** Initializes an instance of `Agent` with `TicTacToeGame`.
- **Training:** Trains the agent (`learn_game`) over 30,000 episodes.
- **Interactive Play:** Offers the user the option to play interactive games against the trained agent.

## Functionality Overview

- **Training:** The agent learns to play Tic Tac Toe by playing against itself using reinforcement learning (Q-learning).
- **Interactive Gameplay:** Users can choose to play Tic Tac Toe against the trained agent, selecting 'X' or 'O'.
- **Statistics:** After training, the code provides statistics on game outcomes (win/draw percentages).
  
      
## Customization

You can experiment with different learning behaviors by modifying parameters such as:
- `epsilon` (exploration rate)
- `alpha` (learning rate)
- Number of training episodes

This setup encapsulates a complete implementation of Tic Tac Toe with a reinforcement learning agent, demonstrating both training and interactive gameplay capabilities. Adjustments can be made for further customization or integration into larger projects.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
