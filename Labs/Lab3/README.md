# Lab 3: The Bellman equations 

In reinforcement learning, the Bellman equations play a fundamental role in understanding and solving Markov decision processes (MDPs). These equations describe how the value function and the action-value function (Q function) of an MDP can be recursively defined in terms of the immediate rewards and the expected future rewards. The Bellman equation of the value function expresses the value of a state as the sum of the immediate reward and the discounted value of the next state, weighted by the probability of transitioning to that state. Similarly, the Bellman equation of the Q function extends this concept to action values, representing the expected return of taking an action in a state and then following a specific policy thereafter. These equations form the basis for many reinforcement learning algorithms, such as value iteration, policy iteration, Q-learning, and deep Q-networks, enabling agents to learn optimal policies in complex environments.

Let's explore the following example to understand how we can apply both the Bellman equation of the value function and the Bellman equation of the Q function to solve it.
Scenario:
# Solving Simple Grid Using Value & Policy Iteration 
## Goal:

Imagine, there is a simple grid world with three states: $S1$, $S2$, and $G$, representing the starting state, an intermediate state, and the goal state, respectively. The agent has two possible actions in each state: left and right. 


1. S1 is the starting position 
2. S2 is the next state
3. G is the Goal (office)

The environment provides a reward of -1 for each step the agent takes, representing the cost of movement, and a reward of +10 for reaching the goal state $G$, representing the final goal achievement.

The discount factor $\gamma$ is set to 0.9, which determines the importance of future rewards relative to immediate rewards. A higher $\gamma$ value indicates that the agent values future rewards more, leading to longer-term planning, while a lower $\gamma$ value gives more weight to immediate rewards, focusing on short-term gains. In this scenario, a $\gamma$ value of 0.9 suggests that the agent considers both short-term and long-term rewards, balancing the trade-off between immediate gains and future benefits.
