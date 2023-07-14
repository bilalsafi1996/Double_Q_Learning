
# Implentation of Double Q-Learning Algorithm

This repository contains an implementation of the Double Q-Learning algorithm for solving the Cliff Walking problem.

# Problem Statement
The Cliff Walking problem is a grid-world problem where an agent needs to navigate from a start state to a goal state while avoiding falling off a cliff. The grid-world is a 4x12 grid, where each cell represents a state. The agent can take four possible actions: North, East, South, and West. However, taking the action "South" in the bottom row will result in falling off the cliff and receiving a large negative reward. The agent receives a reward of -1 for each step taken and a reward of 0 when reaching the goal state.

# Algorithm Description
The algorithm used to solve the Cliff Walking problem is Double Q-Learning. In Double Q-Learning, the agent maintains two separate Q-value functions, QA and QB. The Q-value functions are initialized with zeros and are updated based on the observed rewards and the estimated values of the next state.

The update_Q function is used to update the Q-value functions based on the observed rewards and the estimated values of the next state. The epsilon_greedy_take_action function is used to select actions based on the epsilon-greedy policy, which balances exploration and exploitation. The agent_environment_interaction function handles the interaction between the agent and the environment, including selecting actions, taking steps, and updating the Q-value functions. The cliff_environment function defines the environment dynamics, including the rewards and the transitions between states. The cliff_environment_print_Q and cliff_environment_policy functions are used to print the Q-values and the policy for the Cliff Walking environment.

# Pre-requisites
Make sure you have the following libraries installed:

- numpy
- matplotlib

# Results
The provided code includes an analysis of the training results, including plots of the number of steps and total reward per episode over time. The results show that the agent gradually improves its performance and learns an optimal policy to navigate the Cliff Walking environment.

# Hyperparameter Tuning
The code also includes a section for hyperparameter tuning, where you can evaluate the average reward over a fixed number of episodes for different combinations of epsilon, alpha, and gamma values. This allows you to find the best set of hyperparameters for the Double Q-Learning algorithm.

## References

 -  Hado van Hasselt. Double Q-Learning
 - Richard S. Sutton and Andrew G.Barto. An Introduction to Reinforcement Learning. Chapter 6. Temporal-Difference Learning, page 119-140
 - Prof. Dr. Stefan Faußer. Lecture on Big Data and AI
 