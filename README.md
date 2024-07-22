


# Lunar Lander with Gymnasium and Tianshou

This repository contains the setup and usage instructions for testing the DQN and Double DQN on the Lunar Lander environment using Gymnasium and Tianshou.

## Table of Contents
- [Intro](#Intro)
- [Installation](#installation)
- [Troubleshoot](#Troubleshoot)

## Intro

In this project we used Tianshou and Gymnasium pakages to compare between two RL algorithms - DQN and Double DQN using the Lunar Land Game.
### DQN (Deep Q-Network)
DQN is a reinforcement learning algorithm that combines Q-learning with deep neural networks. It approximates the Q-value function using a neural network, allowing it to handle high-dimensional state spaces. DQN uses experience replay to store and reuse past experiences and a target network to stabilize training.

### Double DQN
Double DQN is an improvement over DQN that addresses the overestimation bias in Q-learning. It uses two separate networks to decouple the action selection from the Q-value evaluation. This leads to more stable and accurate learning by using the main network to select actions and the target network to evaluate those actions.
## Installation

To set up the environment, follow the steps below:

1. **Clone the repository**:
    ```bash
    git clone https://github.com/YuriLizi/LunarLand_RL_course.git
    cd LunarLand_RL_course
    ```
2. **Install python 3.11** (Must use python 3.11 ):
    ```bash
    sudo update-alternatives --install /usr/bin/python python /usr/bin/python3.11 2
    ```
 3. **switch to python 3.11** :
    ```bash
    sudo update-alternatives --config python
   
    ```
    and press 2
     
4. **Create a virtual environment** (optional but recommended):
    ```bash
    python3 -m venv venv
    source venv/bin/activate  
    ```
On Windows, use `venv\Scripts\activate`
5. **Install the required packages**:
    ```bash
    pip install -r requirements.txt
    ```



To install these packages individually:
```bash
pip install gymnasium tianshou
```

3. **Run the training**:

      run "train_dqn.py" for DQN training and run "train_double_dqn.py" for double DQN training


## Troubleshoot
**In case of an error that says you need [box2d] please install the next packages**:
    
```bash
     pip install swig 
     pip install gym[box2d]
```
In case of this error:
```
ModuleNotFoundError: No module named 'tianshou.utils.space_info'
```
Make sure you are using python 3.11 