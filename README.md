# Deep Q-Network (DQN) for CartPole-v1

A Deep Q-Network implementation that teaches an AI agent to balance a pole on a cart through reinforcement learning. The agent learns optimal control strategies by trial and error, achieving superhuman performance in the classic CartPole environment.

## 🎯 Overview

The CartPole problem requires keeping a pole balanced on a movable cart by applying left or right forces. This DQN implementation solves the environment (average reward ≥ 195 over 100 episodes) using advanced reinforcement learning techniques.

## 🧠 Key Features

- **Advanced DQN Algorithm**: Target networks, experience replay, epsilon-greedy exploration
- **State Normalization**: Improves neural network training stability
- **Step-based Learning**: Trains at regular intervals for better sample efficiency
- **Comprehensive Visualization**: Training progress, exploration decay, state statistics
- **Video Generation**: Creates GIF animations of the trained agent

## 🏗️ Architecture

<img width="923" height="206" alt="architecture" src="https://github.com/user-attachments/assets/215f9024-904e-47f7-a2c2-afdb80f2e445" />

### State Features (Input)
- **Cart Position**: Horizontal position of the cart
- **Cart Velocity**: Speed of cart movement
- **Pole Angle**: Angular position of the pole
- **Pole Angular Velocity**: Rate of angular change

### Actions (Output)
- **Action 0**: Apply force to the left
- **Action 1**: Apply force to the right

## 📊 Training Process

1. **Collection Phase** (1500 steps): Random exploration to gather experiences
2. **Training Phase**: Network updates using experience replay every 4 steps
3. **Target Updates**: Copy main network to target network every 1000 steps

## 🔧 Key Components

- **StateNormalizer**: Maintains running mean/variance for stable training
- **DQN**: 3-layer neural network with ReLU activations
- **Agent**: Handles action selection, experience replay, and network updates
- **Visualization**: Comprehensive training analysis and performance metrics

## 📊 Results: 

https://github.com/BasmaZouaoui/carpole-v1-rl-agent/blob/main/training_results.png

**Performance Achieved:**
- **Final Average Reward**: 199.6 (✅ Environment Solved!)
- **Solution Threshold**: 195+ average reward over 100 episodes
- **Training Convergence**: Successfully learned optimal pole balancing strategy
- **Outputs**: `training_results.png` (comprehensive analysis) and `cartpole_trained_agent.gif` (demo video)

## 🚀 Usage

### Prerequisites
```bash
pip install gymnasium numpy torch matplotlib imageio
```

### Running the Training
Open and run the Jupyter notebook (`training.ipynb`). The training will:
1. Train the agent for up to 500 episodes
2. Display progress every 50 episodes  
3. Generate visualization plots
4. Create a performance GIF video
5. Stop early when solved (avg reward ≥ 195)

## 📈 Expected Results

- **Convergence**: Usually solves in 200-400 episodes
- **Performance**: Achieves 400+ step episodes consistently when trained
- **Outputs**: `training_results.png` (plots) and `cartpole_trained_agent.gif` (demo video)
