# DRLND-deep-reinforcement-learning Project 2 Continuous Control
This Repository includes my solution to the Project Continuous control for Udacity's Deep Reinforcement Learning Nanodegree.

# Environment and Statespace
The Projects consists of solving Unitys Reacher Environment which is included in this repository or can be found [for Windows](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip) and here [for Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip) for Linux. 
"""The README describes the the project environment details (i.e., the state and action spaces, and when the environment is considered solved)."""
This 

The environment is considered solvend 
Solve the Second Version
The barrier for solving the second version of the environment is slightly different, to take into account the presence of many agents. In particular, your agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). Specifically,

After each episode, we add up the rewards that each agent received (without discounting), to get a score for each agent. This yields 20 (potentially different) scores. We then take the average of these 20 scores.
This yields an average score for each episode (where the average is over all 20 agents).


# Setting up the environment
For Jupiter workspace: 
Follow the rules of https://github.com/kitu2007/drlnd-deep-reinforcement-learning. 
The following small adjustments can be made in the process.

1. As workspace is on a Ubuntu system (or VM)
conda create --name drlnd python=3.6
source activate drlnd

2. classic control and box2d need not to be installed

3. If it was not done before: 
git clone https://github.com/udacity/deep-reinforcement-learning.git
Then: 
cd deep-reinforcement-learning/python
pip install .

4. 
python -m ipykernel install --user --name drlnd --display-name "drlnd"


full script: 

conda create --name drlnd python=3.6
source activate drlnd
cd deep-reinforcement-learning/python
pip install .
python -m ipykernel install --user --name drlnd --display-name "drlnd"


# Deep Deterministic Policy Gradient (DDPG)

# Parameters

## Plot of Rewards:
The Plot showing an average reward over 16 can be found in Navigation.ipynb .
![Plot also here](/rewards_plot.png)

