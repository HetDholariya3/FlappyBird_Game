🐦 Flappy Bird AI using Deep Q-Network (DQN)

A Reinforcement Learning project that trains an AI agent to play Flappy Bird using the Deep Q-Network (DQN) algorithm implemented with PyTorch and Gymnasium.

📌 Overview

This project uses Deep Reinforcement Learning to teach an agent how to play Flappy Bird by interacting with the environment and learning from rewards.

The agent learns through:

Experience Replay
Epsilon-Greedy Exploration
Target Network Synchronization
Deep Q-Learning (DQN)
🚀 Features
Train an AI agent to play Flappy Bird
Experience Replay Memory
Target Network for stable learning
GPU support using CUDA
Save and load trained models
Human-play mode using keyboard controls

📂 Project Structure
.
├── agent.py                 # Training and testing logic
├── dqn.py                   # Neural network architecture
├── experience_replay.py     # Replay memory implementation
├── game_flappy_bird.py      # Human playable game
├── parameters.yaml          # Hyperparameters
├── runs/
│   ├── flappybirdv0.pt      # Saved model
│   └── flappybirdv0.log     # Training logs
└── README.md

🛠️ Requirements
Python 3.10+
PyTorch
Gymnasium
Flappy Bird Gymnasium
PyGame
PyYAML

Install dependencies:

pip install torch gymnasium flappy-bird-gymnasium pygame pyyaml

Or create a requirements.txt file:

torch
gymnasium
flappy-bird-gymnasium
pygame
pyyaml

Install using:

pip install -r requirements.txt
🎮 Play Flappy Bird Manually

Run:

python game_flappy_bird.py

Controls:

Space Bar → Flap
Close Window → Exit
🏋️ Train the Agent

Run:

python agent.py flappybirdv0 --train

Training information:

Experiences are stored in replay memory.
The policy network learns from sampled experiences.
Best-performing models are automatically saved.

Saved files:

runs/flappybirdv0.pt
runs/flappybirdv0.log

🤖 Test the Trained Agent
After training:
python agent.py flappybirdv0

The trained model will play Flappy Bird automatically.

⚙️ Hyperparameters

Located in parameters.yaml

flappybirdv0:
  epsilon_init: 1
  epsilon_min: 0.05
  epsilon_decay: 0.9995
  replay_memory_size: 100000
  mini_batch_size: 64
  network_sync_rate: 100
  alpha: 0.001
  gamma: 0.99
  reward_threshold: 1000
  
🧠 DQN Architecture
Input Layer (State Space)
        ↓
Linear Layer (256 Neurons)
        ↓
ReLU
        ↓
Output Layer (Q-values)

📈 Reinforcement Learning Concepts Used
Deep Q-Network (DQN)
Bellman Equation
Experience Replay
Epsilon-Greedy Strategy
Target Network
Reward Optimization

💻 GPU Support

The project automatically uses CUDA if available:

if torch.cuda.is_available():
    device = "cuda"
else:
    device = "cpu"
