# Lab: Implementing a Blackjack Environment with Every-Visit Monte Carlo Prediction
## Objective:
To implement an OpenAI Gym environment for playing Blackjack and to use every-visit Monte Carlo (MC) prediction to estimate the state-value function.

## Tasks:
### 1. Implement the Blackjack Environment:

- Create an OpenAI Gym environment for the game of Blackjack using the following rules:
- The game is played with a standard deck of 52 cards.
	- The goal is to get as close to 21 as possible without exceeding it.
	- The dealer plays by a fixed strategy: hitting until the total is at least 17.
- Define the observation space, action space, initial state, and step function for the environment.
### 2. Implement Every-Visit Monte Carlo Prediction:

- Write a function to perform every-visit MC prediction to estimate the state-value function for the Blackjack environment.
- Use a fixed policy (e.g., always stick if the player's sum is 20 or 21, otherwise hit) for generating episodes.
### 3. Testing and Analysis:

Test your Blackjack environment and every-visit MC prediction algorithm by running multiple episodes.
Evaluate the performance of your MC prediction by comparing the estimated state values to the true values (if available).
## Submission:
Submit your Python code for the implemented Blackjack environment and every-visit MC prediction, along with a brief report discussing your implementation, the results of your testing, and any insights or observations.

## Resources:
[The implementation of a blackjack environment with first visit MA](https://github.com/baz2024/DBS_ReinforcementLearning24/blob/main/Labs/Lab%204/4.6%20BlackJack%20with%20First%20visit%20MC.ipynb)
OpenAI Gym documentation: https://gym.openai.com/docs/
Sutton and Barto's "Reinforcement Learning: An Introduction" (Chapter 5) for MC prediction algorithms.
