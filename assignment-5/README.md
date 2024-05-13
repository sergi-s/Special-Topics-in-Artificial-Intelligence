# Reinforcement Learning (RL) Algorithm

In this assignment we implemented a Reinforcement Learning (RL) algorithm for solving problems in a specified environment. Here are the key points about this code:

- **Environment:** The RL algorithm interacts with an environment, represented by a grid or map. The environment provides information about the current state, possible actions, rewards, and transitions.

- **Learning Configuration:** The RL algorithm's learning behavior is determined by configuration settings:
  - `alpha`: Learning rate, which controls how much the algorithm learns from new information.
  - `gamma`: Discount factor, which balances immediate rewards against future rewards.
  - `epsilon`: Epsilon-greedy chance to select a random action, balancing exploration and exploitation.

- **Q-Learning:** The algorithm employs the Q-Learning method, which learns an action-value function that gives the expected utility of taking a given action in a given state.

- **Policy:** The algorithm maintains a policy, which determines the probability of selecting each action in a given state. Initially, the policy may assign equal probabilities to all actions, but it is updated based on Q-values.

- **Learning Iteration:** During each learning iteration, the algorithm performs the following steps:
  1. Selects an action based on the current policy (exploitation) or randomly (exploration).
  2. Observes the next state and reward after taking the action.
  3. Updates the Q-value for the current state-action pair based on the observed reward and the maximum Q-value of the next state.
  4. Updates the policy based on the updated Q-values.

- **Complexity and Importance:**
  - The algorithm's core functionality lies in the `learningIteration` method, where Q-values are updated based on observed rewards and transitions.
  - The policy is updated dynamically to balance exploration and exploitation.
  - Parameters such as learning rate, discount factor, and epsilon play crucial roles in determining the algorithm's performance and convergence.

- **Representation of Grids:** In the grid-based environment, each cell represents a state, and the lines within the cells represent the probability of taking each action (direction) from that state.


## Demo Video

For a visual demonstration of the Reinforcement Learning, please check out the accompanying demo video.

[![Genetic Algorithm for Sudoku](https://img.youtube.com/vi/ycC1cPC5iEM/maxresdefault.jpg)](https://youtu.be/ycC1cPC5iEM)
