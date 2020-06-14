## Semi-gradient TD(0) with State Aggregation

We you will implement **semi-gradient TD(0) with State Aggregation** in an environment with a large state space. The focus is on the **policy evaluation task** (prediction problem) where the goal is to accurately estimate state values under a given (fixed) policy.

Assignment 1. In this assignment we will:

- Implement semi-gradient TD(0) with function approximation (state aggregation).
- Understand how to use supervised learning approaches to approximate value functions.
- Compare the impact of different resolutions of state aggregation, and see first hand how function approximation can speed up learning through generalization.

## Pseudocode

![](data\semi_gradient_td0_for_v.png)

Pseudocode from Sutton & Barto Reinforcement Learning an Introduction page 203.

## Environment

We will implement and use a smaller 500 state version of the problem we covered in lecture (see "State Aggregation with Monte Carlo”, and Example 9.1 in [Sutton & Barto Reinforcement Learning an Introduction](http://www.incompleteideas.net/book/RLbook2018.pdf#page=225)). The diagram below illustrates the problem.

![](data\randomwalk_diagram.png)

There are 500 states numbered from 1 to 500, left to right, and all episodes begin with the agent located at the center, in state 250. For simplicity, we will consider state 0 and state 501 as the left and right terminal states respectively.

The episode terminates when the agent reaches the terminal state (state 0) on the left with -1 reward, or the terminal state (state 501) on the right with +1 reward.