# 🚀 Hybrid MARL + Autoencoder Anomaly Detection

A **hybrid Multi-Agent Reinforcement Learning (MARL)** system for **cybersecurity anomaly detection**.  
Combines:
- **QMIX** (cooperative multi-agent Q-learning)
- **MADDPG** (multi-agent deep deterministic policy gradient)
- **Autoencoder-based anomaly detection** (unsupervised)

Built with **Python**, **Gym**, and **PyTorch**.

---

## 📜 Project Overview

This project simulates a **cyber network** where multiple agents monitor different parts of the system.  
Agents decide whether to:
- Take no action
- Investigate suspicious activity
- Lock down a computer

An **Autoencoder** acts as a *detective*, providing anomaly scores to the agents.  
**QMIX agents** work in cooperation, while a **MADDPG agent** handles independent decision-making.

**Goal:** Catch as many anomalies as possible while minimizing false alarms.

---

## 📁 Project Structure

```text
hybrid-marl-anomaly-detection/
│
├── README.md
├── main.py
├── requirements.txt
├── config.py
│
├── agents/
│   ├── __init__.py
│   ├── base_agent.py
│   ├── qmix/
│   │   ├── __init__.py
│   │   ├── agent.py
│   │   ├── mixer.py
│   │   └── learner.py
│   └── maddpg/
│       ├── __init__.py
│       ├── agent.py
│       ├── critic.py
│       └── learner.py
│
├── detectors/
│   ├── __init__.py
│   └── autoencoder.py
│
├── envs/
│   ├── __init__.py
│   └── cyber_gym.py
│
├── models/
│   ├── __init__.py
│   ├── networks.py
│   └── buffers.py
│
├── utils/
│   ├── __init__.py
│   ├── logger.py
│   └── plotter.py
│
├── scripts/
│   ├── train.py
│   └── eval.py
│
└── tests/
    ├── __init__.py
    ├── test_agents.py
    ├── test_env.py
    └── test_detector.py



```

## ⚙️ Installation

```bash
# Clone repository
git clone https://github.com/DevKhanHassam/CTDE.git
cd hybrid-marl-anomaly-detection
```markdown
# Install dependencies
pip install -r requirements.txt


Dependencies:

torch

numpy

gym

matplotlib

