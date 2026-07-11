# Reinforcement Learning Based Adaptive GUI and Web Automation Agent

## Overview

This project presents an adaptive **Reinforcement Learning (RL)** framework for autonomous interaction with Graphical User Interfaces (GUI) and browser-based applications. The project demonstrates how an RL agent can progressively learn interaction policies, starting from a simple grid-world simulation and ultimately transferring the learned behavior to a real browser environment using **Selenium** and **Deep Q-Networks (DQN)**.

Unlike traditional GUI automation, which relies on hard-coded scripts, the proposed framework enables an agent to **learn through interaction and reward feedback**, making it more adaptable to changing environments.

---

## Project Objectives

* Learn optimal GUI navigation using Q-Learning.
* Adapt to dynamic environments where goals and obstacles change.
* Improve learning speed through Transfer Learning.
* Evaluate robustness under stochastic action execution.
* Extend learning from simulation to browser automation using Deep Reinforcement Learning.
* Demonstrate autonomous execution of a web login workflow.

---

## Project Pipeline

```
Static Grid Environment
        │
        ▼
   Q-Learning Agent
        │
        ▼
Dynamic Environment
        │
        ▼
 Transfer Learning
        │
        ▼
Stochastic Environment
        │
        ▼
 Deep Q-Network (DQN)
        │
        ▼
 Experience Replay
        │
        ▼
 Selenium Browser Automation
        │
        ▼
 Autonomous Login Agent
```

---

## Features

* Custom GUI-inspired Grid World Environment
* Tabular Q-Learning Implementation
* Dynamic Environment Adaptation
* Transfer Learning between environments
* Stochastic Action Execution
* Deep Q-Network (PyTorch)
* Experience Replay Buffer
* Selenium-based Browser Automation
* Simulation-to-Real Policy Transfer

---

## Technologies Used

| Category               | Technologies                     |
| ---------------------- | -------------------------------- |
| Language               | Python                           |
| Reinforcement Learning | Q-Learning, Deep Q-Network (DQN) |
| Deep Learning          | PyTorch                          |
| Browser Automation     | Selenium                         |
| Numerical Computing    | NumPy                            |
| Visualization          | Matplotlib                       |
| Environment            | Jupyter Notebook                 |

---

## Repository Structure

```
.
├── ET Project.ipynb          # Complete implementation
├── README.md                 # Project documentation
├── requirements.txt          # Python dependencies (optional)
└── demo/                     # Screenshots or videos (optional)
```

---

## Methodology

### Phase 1 — Static Grid World

A custom **5 × 5** grid environment simulates GUI components such as buttons, menus, forms, obstacles, and goal states. The agent learns optimal navigation using the Bellman update equation.

---

### Phase 2 — Dynamic Environment

Goal positions and obstacle locations change periodically, forcing the agent to continuously adapt its policy instead of memorizing a fixed path.

---

### Phase 3 — Transfer Learning

The learned Q-table is reused as the initialization for a modified environment. This significantly reduces exploration time compared to training from scratch.

---

### Phase 4 — Stochastic Environment

Random action perturbations simulate uncertainty found in real software interfaces, improving policy robustness.

---

### Phase 5 — Deep Q-Network

The tabular Q-table is replaced by a neural network that approximates the action-value function, allowing the agent to scale to larger state spaces.

---

### Phase 6 — Browser Automation

The learned policy is transferred to a Selenium-controlled login page where the DQN agent autonomously:

* Fills credentials
* Clicks the Login button
* Completes the authentication workflow

---

## Experimental Results

### Transfer Learning

| Metric                             | Transfer Learning | Training from Scratch |
| ---------------------------------- | ----------------: | --------------------: |
| Average Reward (First 50 Episodes) |          **3.36** |                  3.26 |
| Total Reward                       |           **168** |                   163 |

Transfer learning accelerated convergence and improved early-stage learning.

---

### Observations

* Successful policy learning using Q-Learning.
* Robust performance under stochastic actions.
* Faster convergence with Transfer Learning.
* Stable Deep Q-Network training.
* Successful transfer from simulation to browser automation.

---

## Future Improvements

* Visual state representation using CNNs
* DOM-aware state embeddings
* Transformer-based GUI agents
* PPO, Double DQN and Dueling DQN
* Multi-page workflow automation
* Generalized browser interaction

---

## References

1. Sutton, R. S., & Barto, A. G. *Reinforcement Learning: An Introduction (2nd Edition)*.
2. Watkins, C. J. C. H. *Learning from Delayed Rewards*.
3. Mnih, V. et al. *Human-Level Control Through Deep Reinforcement Learning*. Nature, 2015.
4. PyTorch Documentation.
5. Selenium Documentation.

---

## Author

**Niladri Banerjee**

M.Sc. Data Science and Artificial Intelligence
Ramakrishna Mission Vivekananda Educational and Research Institute (RKMVERI), Belur

GitHub: https://github.com/Niladri232

---

## License

This project is developed for academic and research purposes.
