---
layout: project
title: "Saint Petersburg AI Agent"
description: "A tournament-winning AI agent for the board game Saint Petersburg using Monte-Carlo Tree Search and Machine Learning."
image: "/assets/images/st-petersburg-game.webp"
date: 2025-12-01
---

## Project Overview
This project focused on developing an autonomous agent to play the board game *Saint Petersburg*. The goal was not just to play legally, but to optimize decision-making under uncertainty to defeat both heuristic-based opponents and human players.

Our agent achieved **1st Place** in a class tournament.

## Technical Approach

### 1. Monte-Carlo Tree Search (MCTS)
The core decision engine utilizes **MCTS** to explore the game tree MCTS allows the agent to handle the large branching factor of *Saint Petersburg* by prioritizing promising moves.
- **Selection & Expansion:** Used Upper Confidence Bound (UCT) to balance exploration and exploitation.
- **Simulation:** Implemented lightweight random playouts to estimate the value of leaf nodes.

### 2. Machine Learning Evaluation Functions
To improve simulation accuracy beyond random rollouts, I engineered distinct state evaluation models:
- **Logistic Regression (LR):** Trained on game features to predict win probability.
- **Random Forest (RF):** Used for non-linear feature interactions, capturing complex board states.
- **Feature Engineering:** I manually designed features to feed into these models.

### 3. Game Balance Analysis
Beyond the agent, I ran thousands of Monte Carlo simulations to analyze the fairness of the game itself.
- **Findings:** Identified specific cards that were statistically overpowered and underpowered.
- **Output:** Generated a comprehensive **Balance Change Report** recommending adjustments to card costs to ensure competitive fairness.

## Key Technologies
* **Languages:** Java (Core Logic), Python (ML Training)
* **ML Libraries:** scikit-learn (Logistic Regression, Random Forest)
* **Build Tools:** Maven
* **Concepts:** Game Theory, Reinforcement Learning, MCTS

[View Code on GitHub](https://github.com/dannguyen111/saint-petersburg-AIDan-player.git){: .btn .btn-primary .mt-3}
[Read the Balance Change Report (exported from OneNote)](/assets/pdfs/cs391-final-report.pdf){: .btn .btn-primary .mt-3}