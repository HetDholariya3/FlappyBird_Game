# 🐦 Flappy Bird AI using DQN

A Reinforcement Learning project that trains an AI agent to play Flappy Bird using Deep Q-Networks (DQN) with PyTorch and Gymnasium.

## Features

* Deep Q-Network (DQN)
* Experience Replay Memory
* Target Network Synchronization
* GPU (CUDA) Support
* Train and Test Modes

## Installation

```bash
pip install torch gymnasium flappy-bird-gymnasium pygame pyyaml
```

## Train the Agent

```bash
python agent.py flappybirdv0 --train
```

## Test the Agent

```bash
python agent.py flappybirdv0
```

## Project Files

* `agent.py` – Training and testing logic
* `dqn.py` – Neural network model
* `experience_replay.py` – Replay memory
* `game_flappy_bird.py` – Manual gameplay
* `parameters.yaml` – Hyperparameters

## Technologies Used

* Python
* PyTorch
* Gymnasium
* Flappy Bird Gymnasium
* PyGame
