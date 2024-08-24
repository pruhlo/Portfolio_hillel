# Reinforcement learning Project

## Setting Up and Running the Project

1. **Create and Activate Virtual Environment**

   - **Create Virtual Environment**
     ```bash
     python -m venv myenv
     ```
   - **Activate Virtual Environment**
     - On Windows:
       ```bash
       myenv\Scripts\activate
       ```
     - On macOS/Linux:
       ```bash
       source myenv/bin/activate
       ```
   - **Upgrade pip**
     ```bash
     python -m pip install --upgrade pip
     ```
   - **Install Requirements**
     ```bash
     pip install -r requirements.txt
     ```
   - **Run the Game**
     ```bash
     python game.py
     ```
3. **Dependencies**

   All dependencies are listed in the `requirements.txt` file.

## Overview of `game.py`

`game.py` contains code for training and running an agent in the CartPole-v0 environment using the Policy Gradient algorithm. Below is a summary of its functionality:

### Class `Policy`
- Implements a neural network with two fully connected layers.
- Uses a Softmax activation function to choose actions based on the state.

### Class `Runner`
Manages the training and execution process:

- **`select_action(state)`**: Chooses an action based on the current state.
- **`update_policy()`**: Updates the agent’s policy using gradients.
- **`train(episodes, smooth)`**: Trains the agent for a specified number of episodes.
- **`run()`**: Executes the trained agent and saves an animation of its actions.
- **`plot()`**: Creates plots of losses and rewards.
- **`save()`**: Saves the state of the model.
