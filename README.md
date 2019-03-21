# RL1_Navigation
Udacity Deep Reinforcement Learning Nanodegree Program project 1 

The simulation contains a single agent that navigates a large environment. At each time step, it has four actions as following:
- `0` - walk forward 
- `1` - walk backward
- `2` - turn left
- `3` - turn right
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. The goal is to train an smart agent that collect yellow banana while avoid purple banana to achieve a stable high score.

This repository contains 5 files:

- **README.md** - This file prove info for current repository.
- **Nnavigation.ipynb** - This is a fully functional iPython notebook with training score plot. 
- **dqn_agent.py** - This file contains defined function relating to agents.
- **model.py** - This file contains functions that define the training model.
- **checkpoint.pth** - This file contains saved weights for an average score larger than 16.0 for last 100 episode window.

The training method used here is a deep Q-learning with experience replay for a 100 episodes.
