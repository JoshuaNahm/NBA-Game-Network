# DS310 Project: NBA Game Outcomes Analysis

## 📋 Project Overview

This project was conducted to analyze the **betweenness centrality** of NBA teams based on historical game outcomes.

Using data from the 2004 season to the latest available updates, we aimed to uncover which teams play pivotal roles in the connectivity of the NBA game network.


The project was divided into three key modules:

1. **Data Loading & Graph Construction** (construct.rs)

2. **Centrality Computation** (function.rs)

3. **Result Analysis & Visualization** (main.rs)

---

## 📊 Data Sources

- **Game Data:** NBA historical games from Kaggle (2004 - present)

- **CSV File:** games.csv containing team IDs, game results, and win/loss outcomes

---

## ⚙️ Technologies Used

- **Programming Language:** Rust

- **Graph Library:** petgraph

- **Data Handling:** csv and serde crates for CSV parsing and data deserialization

- **Algorithm:** Dijkstra’s algorithm for shortest path calculations

---

## 🚀 Methodology

### 1. **Data Construction** (construct.rs)

- **Input:** games.csv

- **Process:**

  - Reads game outcomes (home/visitor teams, win/loss results)

  - Constructs a **directed graph** where:

    - **Nodes** represent teams

    - **Edges** represent game outcomes (with weights indicating wins)

### 2. **Centrality Calculation** (function.rs)

- **Betweenness Centrality:** Measures how often a team appears on the shortest paths between other teams

- **Algorithm:**

  - Uses **Dijkstra's algorithm** to compute shortest paths

  - Calculates centrality scores based on the frequency of a team being part of these paths

### 3. **Main Program** (main.rs)

- Reads the constructed graph

- Calculates and **sorts** teams based on centrality scores

- **Outputs:** Teams ranked by their importance in the game outcome network

---

## 📈 Results & Key Findings

- **Top Team by Centrality:**

  - **Team ID:** 1610612747

  - **Centrality Score:** 1128.60

  - **Insight:** This team acts as a critical connector in the NBA network, appearing frequently on the shortest paths between other teams.

- **General Observations:**

  - Teams with **higher centrality** have a greater influence on the league’s outcome dynamics.

  - Teams with **lower centrality** have less impact on the overall game flow.

---

## ✅ Test Function

- **Unit Test:** test_sum function ensures the correctness of core functionalities, verifying calculations like vector sums to maintain code reliability.

---

## 🎯 Conclusion

This project demonstrates the power of **graph theory** and **Rust** in sports analytics.

By analyzing the betweenness centrality of NBA teams, we identified key teams that shape the league’s competitive landscape.

The modular design and efficient graph computations using petgraph allow for easy extension to other datasets and sports leagues.
"""
