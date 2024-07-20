# Q Learning
optimal logistic route with Q_learning. Taken from [Udemy AI course](https://www.udemy.com/course/artificial-intelligence-az/)


# Project objective

Given an environment (logistic warehouse with bin areas to pick up references), find the optimal route from a bin X to a bin Y.

We will use Q Learning algorithm.

Option to include intermediate destinations as constraints

The provided environment is the following:

![](asset/environment.png)


# Q Learning implementation
we follow these steps to set up the environment:
- define the set of states - Here the different bins from A to L
- define the set of actions - Here the actions are to move to each of the bin, ie from A to L. Note that not all actions are possible from a given locations. Available actions are dictated by the original environment provided
- define the set of rewards - Here, given a location X, we will assign 1 if the action is feasible, 0 if not. The rewards will be registered in a matrix states x actions. We will assign 1000 as a reward to the destination
