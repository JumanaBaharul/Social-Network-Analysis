# Social Network Analysis

## Overview

This project analyzes three distinct networks:

- **College Message Network**
- **Condensed Matter Collaboration Network**
- **Barabási-Albert (BA) Network (Synthetic)**

The analysis focuses on:

- Network structure
- Centrality measures
- Clustering properties
- Information diffusion using the Independent Cascade Model (ICM)

The project is divided into two rounds:

- **Round 1**: Analysis of the College Message Network and Condensed Matter Collaboration Network, focusing on network statistics, centrality measures, and clustering analysis.
- **Round 2**: Generation and analysis of a Barabási-Albert Network, comparative analysis with the Round 1 networks, and simulation of information diffusion across all three networks.

---

## Datasets

### 1. College Message Network

- **Description**: Temporal directed network of private message exchanges between users in an online social network at the University of California, Irvine.
- **Nodes**: 1,899 users
- **Temporal Edges**: 59,835 messages over 193 days
- **Static Edges**: 20,296 unique edges (ignoring timestamps)

### 2. Condensed Matter Collaboration Network

- **Description**: Undirected network of scientific collaborations between authors in the Condensed Matter category on arXiv (1993–2003).
- **Nodes**: 23,133 authors
- **Edges**: 93,497 collaborations

### 3. Barabási-Albert (BA) Network

- **Description**: Synthetic scale-free network generated using the Barabási-Albert model.
- **Nodes**: 10,000
- **Parameters**:
  - Initial nodes = 100
  - Preferential attachment parameter (m = 3)
- **Generated In-Code**: No separate file; generated using NetworkX.

---

## Methodology

### Round 1: Analysis of Real-World Networks

#### Network Statistics

- Computed basic metrics (number of nodes, edges, mean degree)
- Analyzed degree distribution and clustering coefficients

#### Centrality Measures

- Calculated:
  - Degree Centrality
  - Eigenvector Centrality
  - Katz Centrality
  - PageRank
  - Betweenness Centrality
  - Closeness Centrality
- Identified top 10 nodes for each measure to find influential users/authors

#### Clustering Analysis

- Computed global and local clustering coefficients
- Analyzed reciprocity and transitivity to understand network connectivity

#### Visualization

- Plotted:
  - Degree distributions
  - Centrality distributions
  - Clustering coefficient distributions

### Round 2: Synthetic Network and Comparative Analysis

#### Barabási-Albert Network Generation

- Generated a scale-free network with 10,000 nodes using NetworkX

#### Comparative Analysis

- Compared the BA Network with the College Message and Condensed Matter networks in terms of:
  - Giant component size
  - Mean degree
  - Clustering coefficients

#### Centrality and Clustering

- Applied the same centrality measures and clustering analysis to the BA Network

#### Information Diffusion

- Simulated information spread using the Independent Cascade Model (ICM) on all three networks
- Ran 5 iterations per network to compute average steps to maximum activation

---

## Key Findings

### Network Characteristics

#### College Message Network

- High mean degree (14.57) indicates intensive messaging
- Low clustering (0.109) suggests sparse group interactions
- Influential nodes (e.g., Node 103) dominate communication flow

#### Condensed Matter Collaboration Network

- High clustering (0.633) reflects tight-knit research groups
- Distributed influence with prestigious researchers (e.g., Node 73647)
- Longest diameter (14) indicates slower influence spread

#### Barabási-Albert Network

- Scale-free topology with hub dominance (e.g., Node 8)
- Low clustering due to tree-like structure
- Giant component spans 100% of nodes, ensuring high reachability

### Information Diffusion

- **BA Network**: Limited diffusion (max 9 nodes activated) due to hub dominance; random seeding is ineffective
- **College Message Network**: Rapid but shallow diffusion (14 nodes in 3.6 steps) due to moderate connectivity
- **Condensed Matter Network**: Deeper diffusion (52 nodes in 6.4 steps) but slower due to modular structure

---

## Technologies Used

- Python
- NetworkX
- Matplotlib
- NumPy
- Pandas

---
