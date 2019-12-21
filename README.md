[//]: # (Image References)

[image1]: https://video.udacity-data.com/topher/2018/May/5af7955a_tennis/tennis.png "Trained Agent"

# Project 3: Collaboration and Competition

### Introduction

In this third project two agents control rackets to bounce a ball over a net. The environment is played in a self-play mode, i.e. the trained agent is playing against itself.

![Trained Agent][image1]

An agent receives a reward of +0.1 every time it hits the ball over the net. If an agent lets a ball hit the ground or hits the ball out of bounds, it receives a reward of -0.01. Thus, the goal of each agent is to keep the ball in play for as many hits as possible.

The observation space consists of 8 distinct variables corresponding to the 2-dimensional position and velocity of the ball and the agent's own racket. As 3 subsequent frames are stacked to one observation this amounts to a total of 24 dimensions. Each agent receives its own, local observation. Two continuous actions are available, corresponding to movement toward (or away from) the net, and jumping.

The task is episodic, and in order to solve the environment, the maximum score per episode of either agent must reach an average of +0.5 over 100 consecutive episodes.

### Getting Started

1. If you haven't already, please follow the instructions in the [DRLND GitHub repository](https://github.com/udacity/deep-reinforcement-learning#dependencies) to set up your Python environment. These instructions can be found in README.md at the root of that repository. By following these instructions, you will install PyTorch, the ML-Agents toolkit, and a few more Python packages required to complete the project.

2. Clone this repository.

3. Download the tennis environment from one of the links below. You need only select the environment that matches your operating system:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Windows_x86_64.zip)

    (_For Windows users_) Check out [this link](https://support.microsoft.com/en-us/help/827218/how-to-determine-whether-a-computer-is-running-a-32-bit-version-or-64) if you need help with determining if your computer is running a 32-bit version or 64-bit version of the Windows operating system.

    (_For AWS_) If you'd like to train the agent on AWS (and have not [enabled a virtual screen](https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Training-on-Amazon-Web-Service.md)), then please use [this link](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P3/Tennis/Tennis_Linux_NoVis.zip) to obtain the environment.

4. Place the file in this repository and unzip (or decompress) the file.

### Instructions for Starting to Train the Agent

1. Execute `jupyter notebook` on the CLI at the location you put the repository.

2. Click on `Tennis.ipynb` in the opened browser window to open the notebook containing the training code.

3. Before running the code and thus actually starting the training the link to the tennis environment needs to be changed to fit the exact path to the above downloaded and unzipped tennis environment.

4. Run the code.

The training will stop after either 10,000 episodes or as soon as an average score of +0.5 is achieved over 100 consecutive episodes. The trained actor and critic models are further stored as `stored_model_actor.pth` and `stored_model_critic.pth` at the repository path.