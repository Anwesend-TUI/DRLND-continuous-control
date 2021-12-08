# DRLND-deep-reinforcement-learning Project 2 Continuous Control
This Repository includes my solution to the Project Continuous control for Udacity's Deep Reinforcement Learning Nanodegree.
The following describes the project and how to set up the workspace. The results are described in more detail in `Report.md`.

# Environment and Statespace
The Projects consists of solving Unitys Reacher Environment which is included in this repository or can be found [here for Windows](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip) and [here for Linux](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip) for Linux. 
The version that contains 20 double joint arms in one Unity environment. These arms shall be moved to keep touching a ball. 

## Setting up the environment
For Jupiter workspace: 
Follow the rules of https://github.com/kitu2007/drlnd-deep-reinforcement-learning. 
The following small adjustments can be made in the process.

1. As workspace is on a Ubuntu system (or VM)
conda create --name drlnd python=3.6
source activate drlnd

2. classic control and box2d need not to be installed

3. If it was not done before: 
git clone https://github.com/udacity/deep-reinforcement-learning.git
Then, or if the repository was already cloned: 
cd deep-reinforcement-learning/python
pip install .

4. Create the Jupiter Kernel 
python -m ipykernel install --user --name drlnd --display-name "drlnd"


Full script:  
`conda create --name drlnd python=3.6`  
`source activate drlnd`  
`cd deep-reinforcement-learning/python`  
`pip install .`  
`python -m ipykernel install --user --name drlnd --display-name "drlnd"`

## State and action space look like this
The Action space contains  
Number of agents: 20  
Size of each action: 4  
There are 20 agents. Each observes a state with length: 33  
The state for the first agent looks like: [ 0.00000000e+00 -4.00000000e+00  0.00000000e+00  1.00000000e+00
 -0.00000000e+00 -0.00000000e+00 -4.37113883e-08  0.00000000e+00
  0.00000000e+00  0.00000000e+00  0.00000000e+00  0.00000000e+00
  0.00000000e+00  0.00000000e+00 -1.00000000e+01  0.00000000e+00
  1.00000000e+00 -0.00000000e+00 -0.00000000e+00 -4.37113883e-08
  0.00000000e+00  0.00000000e+00  0.00000000e+00  0.00000000e+00
  0.00000000e+00  0.00000000e+00  5.75471878e+00 -1.00000000e+00
  5.55726624e+00  0.00000000e+00  1.00000000e+00  0.00000000e+00
 -1.68164849e-01]

## The environment is considered solvend 
Solve the Version of the environment with multiple agents the agents must get an average score of +30 (over 100 consecutive episodes, and over all agents). 
So the rewards of each agent are added and the average is taken over all agents after each episode.  

## How to run the code
After setting up the jupyter kernel just execute the `Continuous_Control.ipynb` file. 

