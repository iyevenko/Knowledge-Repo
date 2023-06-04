---
description: This note provides an introduction to NEAT (NeuroEvolution of Augmenting Topologies), an artificial evolution method that uses genetic algorithms to evolve neural networks. It discusses the challenges in NE, NEAT's method, and its contribution to GAs.
---
## NEAT-Python Overview

### Introduction
NEAT (NeuroEvolution of Augmenting Topologies) is an artificial evolution method that uses genetic algorithms to evolve neural networks. It has shown great promise in reinforcement learning tasks and outperforms standard reinforcement learning methods in many benchmark tasks.

### Challenges in NE
One major challenge in NE is how to gain an advantage from evolving topology in addition to connection weights. NEAT addresses this challenge by using a genetic encoding that allows disparate topologies to crossover in a meaningful way. It also protects topological innovation that needs a few generations to optimize by separating each innovation into a different species. Additionally, it minimizes topologies throughout evolution without the need for a specially contrived fitness function that measures complexity.

### NEAT Method
NEAT includes a list of connection genes, each of which refers to two node genes being connected. Each connection gene specifies the in-node, the out-node, the weight of the connection, whether to enable the connection, and a historical marking to line up genes with the same origin.

### Results
NEAT significantly outperforms the fixed-topology NE method on the double pole balancing task, which has been a benchmark task in NE and reinforcement learning for over 30 years. NEAT's performance is due to employing a principled method of crossover of different topologies, protecting structural innovation using speciation, and incrementally growing from minimal structure.

### Contribution to GAs
NEAT is an important contribution to GAs because it shows how it is possible for evolution to both optimize and complexify solutions simultaneously, making it possible to evolve increasingly complex solutions over time, thereby strengthening the analogy with biological evolution.