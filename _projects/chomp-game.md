---
layout: project
title: "Solving 2D Chomp"
description: "Senior Capstone research project solving the 3-row variation of the combinatorial game Chomp."
image: "/assets/images/chomp-diagram.png"
date: 2025-11-01
---

## Research Overview
*Chomp* is a two-player strategy game played on a rectangular chocolate bar. While the game is known to be a "first-player win" for any rectangular size greater than 1x1, finding the explicit winning strategy is an open problem in Combinatorics.

For my **Senior Capstone**, I focused on solving the **3-row variation** of 2D Chomp.

## Methodology

### 1. Computational Proof
I developed a Python-based solver to generate the complete game state graph for fixed board sizes.
- **State Space Search:** Utilized recursive backtracking with memoization to determine Winning (N-position) vs. Losing (P-position) states.
- **Optimizations:** Implemented Zobrist Hashing to efficiently store and retrieve board evaluations, reducing computation time for larger N.

### 2. Mathematical Analysis
Beyond brute force, I analyzed the patterns in the winning moves (kernel elements).
- Investigated the relationship between row lengths and losing positions.
- Verified known results for $2 \times N$ boards and extended analysis to $3 \times N$ configurations.

## Impact
This project contributes to the understanding of impartial combinatorial games. The solver provides a tool for verifying theoretical conjectures and visualizing the "kernel" of the game.

## Tools Used
* **Language:** Python
* **Concepts:** Combinatorial Game Theory, Graph Theory, Dynamic Programming, Memoization