# Lab Exercise: Solving a Gym Environment using the Bellman Equation

## Objective: To apply the Bellman Equation to solve a Gym environment.

**Task:** Use the Bellman Equation to find the optimal value function and policy for a different environment in Gym, such as the CartPole-v1 environment.

## Instructions:

1. Load the CartPole-v1 environment from Gym.
1. Implement the Bellman Equation to update the value function iteratively until convergence.
1. Use the updated value function to derive the optimal policy.
1. Test the optimal policy in the environment to see if the agent can successfully balance the cartpole.
## Hints:

- Use the gym library to create and interact with the CartPole-v1 environment.
- Implement the Bellman Equation update step as a function that takes the current value function, transition probabilities, rewards, and discount factor as inputs.
- Use numpy arrays to represent the value function, transition probabilities, and rewards.
- Iterate the Bellman Equation update until the values converge (i.e., the change in values is below a certain threshold).
## Expected Output:

1. The optimal value function for each state in the CartPole-v1 environment.
1. The optimal policy derived from the optimal value function.
1. Visualization or simulation of the agent balancing the cartpole using the optimal policy.
**Submission:** Submit your code implementation along with a summary of the steps taken to apply the Bellman Equation and the results obtained to Moodle

## Challenge Task: Solving a Gym Environment using the Bellman Optimality Equation

**Objective:** To apply the Bellman Optimality Equation to solve a Gym environment.

**Task:** Use the Bellman Optimality Equation to find the optimal value function and policy for the CartPole-v1 environment in Gym.

## Instructions:

1. Load the CartPole-v1 environment from Gym.
1. Implement the Bellman Optimality Equation to update the value function iteratively until convergence.
1. Use the updated value function to derive the optimal policy.
1. Test the optimal policy in the environment to see if the agent can successfully balance the cartpole.
## Hints:

- Use the gym library to create and interact with the CartPole-v1 environment.
- Implement the Bellman Optimality Equation update step as a function that takes the current value function, transition probabilities, rewards, and discount factor as inputs.
- Use numpy arrays to represent the value function, transition probabilities, and rewards.
- Iterate the Bellman Optimality Equation update until the values converge (i.e., the change in values is below a certain threshold).
## Expected Output:

- The optimal value function for each state in the CartPole-v1 environment.
- The optimal policy derived from the optimal value function.
- Visualization or simulation of the agent balancing the cartpole using the optimal policy.
