---
layout: project
title: "Computational Analysis of 3xN Chomp"
description: "A computational research project identifying infinite families of P-positions in the 3-row game of Chomp."
image: "/assets/images/chomp-diagram.jpg"
date: 2025-11-24
---

## Research Overview
*Chomp* is an impartial combinatorial game played on a grid. While the winning strategy for $2 \times n$ boards is well-known, the $3 \times n$ case remains unsolved in closed form.

For my **Senior Capstone**, I bridged the gap between theoretical existence and practical strategy. Instead of relying on Sprague-Grundy values, I focused on identifying structural patterns directly within the set of **P-positions** (losing positions).

## Methodology

### 1. Recursive Solver & Memoization
I implemented a recursive backtracking solver in **Python** to exhaustively map the game's state space.
- **State Representation:** Modeled the board as a tuple of integers $(r_1, r_2, r_3)$ corresponding to Young's Diagrams.
- **Memoization:** Utilized a hash map to cache the win/loss status of every visited state, allowing me to analyze board widths up to $n=500$ despite the $O(n^3)$ state space growth.

### 2. Pattern Discovery
By analyzing the density and distribution of P-positions, I discovered that for specific fixed third-row lengths ($r_3$), the P-positions settle into predictable arithmetic progressions.

## Key Findings

### 1. Infinite Linear Families
The central contribution of this work was the formal proof of infinite linear families of P-positions. I proved by **mathematical induction** that the following positions are losing states for all non-negative integers $a$:
- **Family 1 ($r_3=2$):** $(a+4, a+2, 2)$
- **Family 2 ($r_3=5$):** $(a+11, a+7, 5)$

### 2. The "Gap Principle"
Based on the data, I introduced the **Gap Principle Conjecture**, hypothesizing that if a fixed third-row length $k$ admits an infinite linear family, then $r_3 = k+1$ cannot. This observation aligns with Byrnes' periodicity theorems.

### 3. Optimal Opening Moves
I analyzed the unique winning move from the starting position $(n, n, n)$. My data suggests a strict dichotomy where the optimal move is either to the second row or the third row (never both), partitioning the integers into two disjoint sets.

## Tools & Technologies
* **Language:** Python
* **Concepts:** Combinatorial Game Theory, Young's Diagrams, Dynamic Programming
* **Output:** LaTeX Research Paper

[Read the Full Paper](/assets/pdfs/capstone_paper_final.pdf){: .btn .btn-primary .mt-3}