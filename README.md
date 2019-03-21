# RL1_Navigation
Udacity Deep Reinforcement Learning Nanodegree Program project 1 

## Environment explained
The simulation contains a single agent that navigates a large environment. At each time step, it has four actions as following:
- `0` - walk forward 
- `1` - walk backward
- `2` - turn left
- `3` - turn right
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. The goal is to train an smart agent that collect yellow banana while avoid purple banana to achieve a stable high score. The environment is consider solved when the average score of last 100 episodes is higher than 16.

## Files in the repository
This repository contains 5 files:

- **README.md** - This file prove info for current repository.
- **Nnavigation.ipynb** - This is a fully functional iPython notebook with training score plot. 
- **dqn_agent.py** - This file contains defined function relating to agents.
- **model.py** - This file contains functions that define the training model.
- **checkpoint.pth** - This file contains saved model weights for an average score larger than 16.0 for last 100 episode window.

The training method used here is a deep Q-learning with experience replay for a 100 episodes.

## To excute the codes
The code relay on a **Banana.exe** evironment for training and verification. Set up the Python 3.6 environment, and change the **env** to your local **Banana.exe** file path, then the file should be functional. 

### Getting Started
1. Download the environment the link below (For this project I used Linux)
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)

2. Place the file in the root folder of the repo and decompress it.

## Instructions

#### Install requirements:
Create a new environment with Python 3.6 in Anaconda promopt.
```
conda create --name drlnd python=3.6 
activate drlnd  
```
#### Dependencies
Clone the repository, and navigate to the *python/* folder. Then, install several dependencies.
```
git clone https://github.com/udacity/deep-reinforcement-learning.git
cd deep-reinforcement-learning/python
pip install .
```

####
Create an *IPython* kernel for the drlnd environment.
```
python -m ipykernel install --user --name drlnd --display-name "drlnd"
```
#### Train the agent
Open an Anaconda prompt and do following:
```
ipython notebook Navigation.ipynb
```
