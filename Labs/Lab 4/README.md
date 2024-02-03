# Lab 4: Monte Carlo Methods

The Monte Carlo method is a statistical technique used to find an approximate solution
through sampling.
1.
It is commonly used in design and engineering to simulate a wide range of scenarios and
help identify the most optimal solution.
2.
The Monte Carlo method involves generating random inputs within specified ranges and
running simulations to calculate the probable output based on those inputs.
3.
It is particularly useful when dealing with complex systems or problems with many variables.
4.
The method is named after the famous casino in Monte Carlo, as it relies on probability and
chance in a similar way to gambling.
5.
By using the Monte Carlo method, designers can make informed decisions based on data-
driven insights and reduce the risk of costly errors in their designs.
6.
The Monte Carlo method approximates the expectation of a random variable by sampling, with
better approximations resulting from larger sample sizes. To compute the expected value of a
random variable X, the sum of the values of X multiplied by their respective probabilities is taken
Let's explore the following example to understand how we can apply both the Bellman equation of the value function and the Bellman equation of the Q function to solve it.
Scenario:
# Solving Simple Grid Using Monte Carlo Methods
## Goal:

Consider a 3x3 grid where the agent can move left, right, up, or down. The grid has a reward of −1 for each step, and the agent receives a reward of +10 for reaching the goal state. The discount factor γ is set to 0.9. We’ll use the first-visit Monte Carlo method to estimate the value function.
In this Lab we can find the following examples:
1. Example: Monte Carlo Method for Grid World

In This Lab we can find the following resources
1.  BlackJack with First visit MC
2.  Estimating Value of Pi using Monte Carlo
3. BlackJack with Epsilon-greedy MC

