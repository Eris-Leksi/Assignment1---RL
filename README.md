# Assignment 1 — Reinforcement Learning (MDPs, Value Iteration, Monte Carlo)

This repository contains solutions for **Assignment 1** of the Reinforcement Learning course.  
It covers formulating MDPs, applying Value Iteration in different gridworlds, and implementing Off-Policy Monte Carlo with Importance Sampling.


---

## 📝 Problem Statements & Solutions

### **Problem 1 [10 pts] — Pick-and-Place Robot**
- **Task:** Formulate the pick-and-place robot arm control problem as a Markov Decision Process (MDP).
- **MDP Design:**
  - **States (S):** Positions and velocities of robot joints/linkages.
  - **Actions (A):** Motor torque/velocity commands.
  - **Rewards (R):** Positive reward for smooth, fast placement. Negative reward for jerky or slow movements.
- **Reasoning:** This representation ensures the agent learns smooth trajectories directly from low-level motor control feedback.

---

### **Problem 2 [20 pts] — 2x2 Gridworld**
- **Environment:**
  - States: \(s_1, s_2, s_3, s_4\)  
  - Actions: up, down, left, right  
  - Rewards: \(R(s_1)=5, R(s_2)=10, R(s_3)=1, R(s_4)=2\)  
  - Initial policy: always move **up**.
- **Tasks:**
  - Perform **two iterations** of Value Iteration (manual, no code).
  - Show:
    1. Initial value function
    2. Updates after Iteration 1
    3. Value function after Iteration 2
- **Deliverables:** Step-by-step tables of \(V(s)\) and the updated policies.

---

### **Problem 3 [35 pts] — 5x5 Gridworld**
- **Environment:**
  - States: \(s_{i,j}\) for rows/columns
  - Goal: \(s_{4,4}\) (reward = +10, terminal)
  - Grey states: \(s_{1,2}, s_{3,0}, s_{0,4}\) (reward = -5)
  - Other states: reward = -1
- **Tasks:**
  1. Implement **standard Value Iteration** to compute \(V^*\) and \(\pi^*\).
  2. Implement **In-Place Value Iteration** (update values immediately in the same array).
  3. Compare:
     - Optimal value function and policies
     - Optimization time
     - Iterations/episodes
     - Computational complexity
- **Deliverables:**  
  - Code with comments  
  - Tables/figures for \(V^*\) and \(\pi^*\)  
  - Discussion of efficiency and complexity

---

### **Problem 4 [35 pts] — Off-Policy Monte Carlo with Importance Sampling**
- **Environment:** Same 5x5 gridworld from Problem 3.
- **Tasks:**
  1. Generate episodes using a **random behavior policy**.
  2. Estimate returns using **discount factor** \( \gamma = 0.9 \).
  3. Apply **importance sampling** to update the value function.
  4. Derive a greedy target policy from the estimates.
- **Deliverables:**
  - Full code (with comments)
  - Estimated value function \(V_{\text{MC}}\)
  - Comparison with \(V^*\) from Value Iteration:
    - Optimization time
    - Number of episodes
    - Computational complexity
    - Policy quality

---
