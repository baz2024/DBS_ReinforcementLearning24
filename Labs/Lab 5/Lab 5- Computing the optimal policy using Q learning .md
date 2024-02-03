# Lab: Computing the Optimal Policy using Q-Learning and SARSA
## Introduction
In this lab, you will write an OpenAI Gym environment for a custom grid world problem and implement the Q-learning and SARSA algorithms to compute the optimal policy for navigating the grid world. The goal is to understand how these reinforcement learning algorithms can be applied to solve a simple yet customizable environment.

## Task
### 1. Environment Setup:

Define a grid world environment with customizable dimensions, starting position, goal position, and possible actions (e.g., up, down, left, right).
Implement the step() function to simulate agent movements based on the chosen action.
Define the rewards for different states and actions according to the problem requirements (e.g., -1 for each step, +10 for reaching the goal).
Implement the reset() function to reset the environment to its initial state.
### 2. Q-Learning:

Implement the Q-learning algorithm to learn the optimal policy for the grid world.
Update the Q-values based on the observed transitions and rewards using the Q-learning update rule.
Use an ε-greedy policy for exploration and exploitation.
### 3. SARSA:

Implement the SARSA algorithm to learn the optimal policy.
Update the Q-values based on the observed transitions and rewards using the SARSA update rule.
Use an ε-greedy policy for exploration and exploitation.
### 4. Evaluation:

Run multiple episodes of Q-learning and SARSA to observe how the algorithms learn and converge to the optimal policy.
Compare the performance of Q-learning and SARSA in terms of convergence speed and final policy quality.
## Submission Guidelines
- [x] Write a Python script or Jupyter Notebook that includes your implementation of the grid world environment, Q-learning, and SARSA algorithms.
- [x] Include comments and explanations to describe your implementation choices and the behavior of the algorithms.
- [x] Run experiments with different parameters (e.g., learning rate, discount factor, exploration rate) and discuss their impact on the algorithms' performance.
- [x] Submit your script or notebook along with a brief report discussing your findings and observations.
## Resources
- OpenAI Gym documentation: https://gym.openai.com/docs/
- Reinforcement Learning: An Introduction by Richard S. Sutton and Andrew G. Barto (Chapter 6 for Q-learning and SARSA)
