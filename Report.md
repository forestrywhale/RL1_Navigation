# simulation report

### Environment explained
The simulation contains a single agent that navigates a large environment. At each time step, it has four actions as following:
- `0` - walk forward 
- `1` - walk backward
- `2` - turn left
- `3` - turn right
The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction. A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana. The goal is to train an smart agent that collect yellow banana while avoid purple banana to achieve a stable high score. The environment is consider solved when the average score of last 100 episodes is higher than 16.

### Learning Algorithm
The learning algorithm used here is deep Q-learning method with fixed Q-targets and experience replay.
The algorithm steps can be described as following:
- 1 - The algorithm initiate all action values to 0.
- 2 - The agent choose an action a1 according to epsilon-greedy probabilities. The epsilon-greedy policy allow the algorithm search action space based on maximized action value as well as a random choice with a probability decided by epsilon and the action space size. 
- 3 - With the returned reward R1 and state S1, update the action value for state S1 with a maximized action value corresponding to an action. 
- 4 - After updating the action value table, which is a Q-table, go back to step 2 till reach the training goal or the maximum training episodes. 

### Network architecture
There is 2 linear transformation layer with relu activation, and a final linear transformation output layer. 

### Hyperparameters
- BUFFER_SIZE = int(1e5)     # replay buffer size
- BATCH_SIZE = 64            # minibatch size
- GAMMA = 0.99               # discount factor
- TAU = 1e-3                 # for soft update of target parameters
- LR = 5e-4                  # learning rate
- UPDATE_EVERY = 4           # how often to update the network
- n_episodes = 2000          # number of max episode for the algorath training 
- mmax_t = 1000              # the maximus training steps for an episolde
- eps_start = 1.0            # the starting epsilon value
- eps_end = 0.01             # the ending epsilon value
- eps_decay = 0.995          # epsilon decay coefficient


### Plot of Rewards
Here is the scoring plot. The x-axis is number of episodes. The y-axis is the cumulative score for the episodes. 
![Training Score Plot](https://github.com/kikyo91/RL1_Navigation/blob/master/score.png)

### Ideas for Future Work
Training with biased data may miss the right solution for rare events. Thus we can try the Prioritized Experience Replay. This method tuning parameters for a modified update rule.
The over estimation might be corrected by double DQN that have an additional evaluation step.
Dueling DQN, which is combining direct estimation of parameters and an advantagous values to the final output. This architecture is useful when some states action pair contributing to the final results only on rare cases.
Further, if we combine all methods described above, called rainbow algorithm, we might be able to get a better predition.
