[image1]: ./data/navigation_episodes_required.png "Episode required"

[image2]: ./data/navigation_reward_per_episode.png "Reward per episode"
# Introduction

1. The objective of this project was to train a Unity ML agent whose goal is to navigate and collect bananas in a square enivronment where the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas. 
2. Acceptance criteria was to traina an agent thay produce a score of greator than +13 over 100 consecutive episodes.
3. I have used Deep Q networks to train the agent till the average reward over 100 consecutive episodes does reach 15.
4. This report contains brief desciption of the algorithm we have used for the training, the architecture and the hyperparameters used.
5. It also conatins he result of the trained agent, graph of reward vs episodes.


# General desciption of Deep Q networks - 

- `Q-learning` learns the action-value function Q(s, a): how good to take an action at a particular state. In Q-learning, we build a memory table Q[s, a] to store Q-values for all possible combinations of s and a.

- However, if the combinations of states and actions are too large, the memory and the computation requirement for Q will be too high. To address that, we switch to a deep network Q (DQN) to approximate Q(s, a). The learning algorithm is called Deep Q-learning. 

- In `deep Q-learning`, we use a neural network to approximate the Q-value function. The state is given as the input and the Q-value of all possible actions is generated as the output

- One of the interesting things about Deep Q-Learning is that the learning process uses 2 neural networks. These networks have the same architecture but different weights. Every N steps, the weights from the main network are copied to the target network. Using both of these networks leads to more stability in the learning process and helps the algorithm to learn more effectively. In our implementation, the main network weights replace the target network weights every `4 steps`.

# Implementation

## 1. Neural Network achitecture used -

I tried a bunch of achitecture with 3 hidden layers and different number of neurons, but the architecture that worked the best was the following - 

1. I have used a multi layed neural network with 2 hidden layers of 64 neurons each.
2. The input layer takes a 37 dimensional vector corresponding to current state in environment while the output layer has 4 neurons corresponsing to 4 possible actions.
2. The after every layer I use a ReLU activation function except for after the output layer.

## 2. Hyperparameters used

- Max number of episodes - 1800
- Max timesteps - 750
- eps_start =1 (Beginning Epsilon value used in e-greedy policy
- eps_End =0.01 (Lower Limit Epsilon value used in e-greedy policy
- eps_Decay = 0.995 (factor by which Epsilon value gets reduced
- BUFFER_SIZE = int(1e5) (replay buffer size)
- BATCH_SIZE = 128
- GAMMA= 0.99 (Discount Rate)
- LR = 1e-3 (learning rate)
- TAU = 1e-3 (for soft update of target parameters)

# Result (Reward per episode graph)

- I was able to achieve a average score of 15.02 over 100 consecutive episodes in 514 episodes.

![Episode required][image1]
- Reward per episode graph - 

![Reward per episode][image2]


# Conclusion
1. I used a larger learning rate of 1e-3 and a larger batch size than the defaults and reduced the max timesteps to 750 for less traning time.
2. These combinations seemed to work well and I was able to pass the acceptance criteria of +13 averaged reward in 100 consecutive time steps.

# Ideas for future work - 

1. There are many optimizations for DQN available to use, I would like to use all rainbow optimization.

- Double Deep Q-Network
- Prioritized Experience Replay
- Duelling Deep Q-Network
- Mulit-step Bootstrap Tragets
- Distributional Deep Q-network
- Noisy Deep Q-Network

2. I would also like to use CNN using the raw pixels as the input data and see if I can improve on these results.






