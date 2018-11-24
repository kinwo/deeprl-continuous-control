# Continuous Control using Deep Reinforcement Learning on Unity ML Agent

## Introduction
This repository contains a Deep Deterministic Policy Gradients (DDPG) agent running in the Unity ML Agent Reacher(https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Learning-Environment-Examples.md#reacher) environment. It can be used to train and evaluate the result of the training.

I use it for the purpose of learning DDPG agent in the context of continuous control of a agent.

The DDPG is implemented in Python 3 using PyTorch.

The full report can be found here. (https://github.com/kinwo/deeprl-continuous-control/blob/master/Report.pdf)

### Environment
The 3D environment contains 20 double joined arms agents who can move freely to reach the target locations.

### Goal
The goal is to control the 20 arms to move to their individual target locations and keep them there as many time steps as possible.

### Environment Solved Criteria
 The environment is considered solved when the average mean score of all agents reach 30+ in the last 100 epsisodes.
 
### Rewards
A reward of +0.1 is provided for each step that each agent's hand is in the goal location independently.

### Actions
Vector Action space: (Continuous) Size of 4, corresponding to torque applicable to two joints.

### Spaces
The observation space is composed of 33 variables:  
position, rotation, velocity, and angular velocities of the arm

## Getting Started
1. Install Unity ML
https://github.com/Unity-Technologies/ml-agents/blob/master/docs/Installation.md

2. Download the Unity ML environment from one of the links below based on your OS:
    - Linux: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Linux.zip)
    - Mac OSX: [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher.app.zip)
    - Windows (32-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86.zip)
    - Windows (64-bit): [click here](https://s3-us-west-1.amazonaws.com/udacity-drlnd/P2/Reacher/Reacher_Windows_x86_64.zip)

Then unzip the file and place the file in this project folder.

3. Create Conda Environment   

Install conda from conda.io. Create a new Conda environment with Python 3.6.

```bash
conda create --name deeprl python=3.6
source activate deeprl
```

4. Install Dependencies
```bash
cd python
pip install .
```


## How to run the agent
To start training, simply open *Continuous_Control.ipynb* in Jupyter Notebook and follow the instructions there:

Start Jupyter Notebook
```bash
jupyter notebook
```
Trained model weights is included for quickly running the agent and seeing the result in Unity ML Agent.
Simply skip the training step and run the last step of the *Continuous_Control.ipynb*
