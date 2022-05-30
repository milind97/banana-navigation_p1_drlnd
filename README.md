# Deep reinforcement learning project 1

[image1]: https://user-images.githubusercontent.com/10624937/42135619-d90f2f28-7d12-11e8-8823-82b970a54d7e.gif "Trained Agent"



# Introduction
This project is part of Udacity Deep Reinforcement Learning Nanodegree. In this project we will train a agent to navigate and collect banana using Unity ML environment.

![Trained Agent][image1]

# Objective of the project - 
A reward of +1 is provided for collecting a yellow banana, and a reward of -1 is provided for collecting a blue banana.  Thus, the goal of your agent is to collect as many yellow bananas as possible while avoiding blue bananas.

The task is episodic, and in order to solve the environment, your agent must get an average score of +13 over 100 consecutive episodes.

## State Space - 

The state space has 37 dimensions and contains the agent's velocity, along with ray-based perception of objects around agent's forward direction.  Given this information, the agent has to learn how to best select actions.  

## Action space - 

Four discrete actions are available, corresponding to:
- **`0`** - move forward.
- **`1`** - move backward.
- **`2`** - turn left.
- **`3`** - turn right.

# Requirements - 

1. First requirement to run this project is to setup drlnd repository. Follow the instructions mentioned on their github repository - [link](https://github.com/udacity/deep-reinforcement-learning#dependencies)

2. After creating a new environment and installing drlnd repository and its dependencies, clone this repo and run the following command to install all the python libraries.

```bash
git clone https://github.com/milind97/banana_navigation_p1_drlnd.git
cd banana_navigation_p1_drlnd
pip install -r requirement.txt
```
3. After this you will also need Unity ML agents environment for the simulation to run. Download the environment from one of the links below.  You need only select the environment that matches your operating system
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Windows_x86_64.zip)
    
    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P1/Banana/Banana_Linux_NoVis.zip) to obtain the environment.
4. Place the downloaded file into "data" folder for this repository.


# Project Structure - 

- src
    - navigation_agent.py
    - navigation_model.py
- data
    -  model_weights.pth
- Navigation.ipynb
- README.md
- Report.md


This repository contains 2 folders - 
1. `src` - This folder has all the required code to train the agent.
2. `data` - This folder contains the saved model weights for the trained agent.
3. Navigation.ipynb - This jupyter notebook has codes to train the agent using Deep Q networks and to runt he trained agent.
4. README.md - Contains intructions to use this repository
5. Report.md - Contains information about the algorithm used to train the agent.

# Steps to run it

1. Install all the dependencies and run the cells in Navigation.ipynb jupyter notebook.



