# GL Code Matching Algorithms

This repository contains three different algorithmic implementations to match General Ledger (GL) codes based on shipment data. The implementations include:

1. **Graph-Based Algorithm**
2. **Trie-Based Algorithm**
3. **Nested Loops Algorithm**

## Algorithms Overview

### 1. Graph-Based Algorithm
This algorithm uses a graph structure where GL codes and their associated parameters are represented as nodes. Edges between nodes carry weights, which are used to determine the best match for a given shipment query.

- **Implementation:** Nodes represent GL codes and parameters (e.g., `source_code`, `tariff`). Edges between parameter nodes and GL code nodes are weighted. The best GL code is found by traversing the graph and summing weights.

### 2. Trie-Based Algorithm
The Trie (prefix tree) algorithm stores GL codes in a hierarchical structure, where each level represents a parameter in the shipment data. This structure allows for efficient storage and retrieval.

- **Implementation:** Parameters are stored as nodes in a trie, and GL codes are stored at the leaves with accumulated weights.

### 3. Nested Loops Algorithm
A simple and straightforward approach that uses nested loops to compare each GL code against the shipment query. It checks all possible combinations and returns the GL code with the highest matching score.

- **Implementation:** For each GL code, the algorithm iterates through all parameters and checks for matches against the query, accumulating the weights.
