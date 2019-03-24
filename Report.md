# simulation report

## Environment explained
The simulation contains a single agent that navigates a large environment. At each time step, it has four actions as following:
- `0` - walk forward 
- `1` - walk backward
- `2` - turn left
- `3` - turn right
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. The goal is to train an smart agent that collect yellow banana while avoid purple banana to achieve a stable high score. The environment is consider solved when the average score of last 100 episodes is higher than 16.

## Learning Algorithm
The learning algorithm used here is deep Q-learning method.

#### Q-Learning (or Sarsamax)
/epsilon


## Hyperparameters


## Plot of Rewards
Here is the scoring plot. The x-axis is number of episodes. The y-axis is the cumulative score for the episodes. 
![Training Score Plot](https://github.com/kikyo91/RL1_Navigation/blob/master/score.png)

## Ideas for Future Work
