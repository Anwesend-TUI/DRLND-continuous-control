# Learning Algorithm

## Deep Deterministic Policy Gradient (DDPG)

## Parameters
BUFFER_SIZE = int(1e6)  # replay buffer size
BATCH_SIZE = 256        # minibatch size
GAMMA = 0.99            # discount factor
TAU = 1e-3              # for soft update of target parameters
LR_ACTOR = 1e-3         # learning rate of the actor 
LR_CRITIC = 2e-3        # learning rate of the critic
#LR_ACTOR = 1e-4         # learning rate of the actor 
#LR_CRITIC = 3e-4        # learning rate of the critic
WEIGHT_DECAY = 0.00001   # L2 weight decay
UPDATE_INTERVAL = 20
LEARN_PASSES=10
EPSILON=1
EPSILON_DECAY=1e-6 

Particularly important and with serious implications was the selected seed parameter. Here in my case `seed = 3` lead to good training results, whereas values like e.g. 1, 2 or 541 ... did not. 

# Plot of Rewards:
The Plot showing an average reward over 30 can be found in Continuous_Control.ipynb and here ![Plot of the Results](Training_results.png).
With Episode 21 the reward was the first time bigger than 30. The following consecutive 100 episodes were also each with rewards >=30. So the training was successfully stopped after episode 121.

# Ideas for Future Work:
Tuning the DDPG algorithm required a lot of trial and error. Especialy the dependency on the random seed was a downside in my opinion. So more research should be done on how this dependency on a randomnes at the initialization can be reduces. Probably for this task/application other reinforcement learning algorithms are more beneficial. 
Perhaps another algorithms like [Proximal Policy Optimization (PPO)](Proximal Policy Optimization Algorithms), or Distributed Distributional Deterministic Policy Gradients (D4PG) would be more robust.

Maybe in the learning step, when the buffer is filled to a certain amount (for example 1/4 or 1/3) not just randomly select episodes from the replay buffer, but instead search for episodes that had a reward > a certain reference value. I think this is called prioritized experience replay.

