---
layout: project
title: "Mancala AI Agent"
description: "A competitive AI agent for the game of Mancala using Minimax search and Alpha-Beta pruning."
image: "/assets/images/mancala-board.jpg"
date: 2025-02-01
---

## Project Overview
This project involved designing and implementing an autonomous agent to play the ancient board game *Mancala* (specifically the Kalah variation). The goal was to create a bot capable of defeating both human players and other AI agents in a class tournament setting.

The agent was built in **Java** and focused on optimizing adversarial search algorithms to make the best decision within strict time constraints.

## Technical Approach

### 1. Adversarial Search Engine
The core of the agent is a **Minimax** algorithm enhanced with **Alpha-Beta Pruning**.
- **Search Optimization:** By pruning irrelevant branches of the game tree, the agent could search significantly deeper than a standard Minimax implementation, allowing it to foresee traps and set up multi-turn captures.
- **Iterative Deepening:** To handle the tournament's strict time limits per move, I implemented iterative deepening. The agent searches to depth $d$, returns a "best guess," and then attempts depth $d+1$. If the timer runs out, it immediately returns the best move found so far.

### 2. Heuristic Evaluation
Since exploring the entire game tree is impossible in the middle game, I engineered a heuristic function to estimate the value of non-terminal states.
- **Score Difference:** The primary driver was the difference between the agent's store and the opponent's store.
- **Positional Factors:** The heuristic also rewarded states that granted "free turns" (landing in the store) and penalized states that left the agent vulnerable to captures.

### 3. Dynamic Time Management
I developed a `Stopwatch` utility to manage the agent's resources. The searcher dynamically monitors elapsed time during recursion and halts execution safely to ensure the agent never forfeits a turn due to timeout.

## Key Technologies
* **Language:** Java
* **Algorithms:** Minimax, Alpha-Beta Pruning, Iterative Deepening DFS
* **Concepts:** Game Theory, Heuristics, Object-Oriented Design

[View Code on GitHub](https://github.com/dannguyen111/dansing_fairkalah){: .btn .btn-primary .mt-3}