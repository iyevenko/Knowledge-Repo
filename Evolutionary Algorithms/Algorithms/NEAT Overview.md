---
description: An overview of the NEAT (NeuroEvolution of Augmenting Topologies) algorithm, which is an evolutionary algorithm that evolves artificial neural networks with the ability to grow and change their structure over time. The note discusses how NEAT protects innovation through speciation, matches up genomes for different network topologies, minimizes dimensionality, and efficiently searches for solutions.
---
## NEAT Overview

### Introduction
NEAT (NeuroEvolution of Augmenting Topologies) is a type of evolutionary algorithm that evolves artificial neural networks (ANNs) with the ability to grow and change their structure over time. 

### Protecting Innovation through Speciation
NEAT speciates the population, so that individuals compete primarily within their own niches instead of with the population at large. This way, topological innovations are protected and have time to optimize their structure before they have to compete with other niches in the population. 

### Matching up Genomes for Different Network Topologies
NEAT uses innovation numbers to match up genomes for different network topologies. This allows for the identification of which genes match up with which without the need for topological analysis.

### Minimizing Dimensionality
NEAT begins with a uniform population of networks with no hidden nodes. Because NEAT protects innovation using speciation, it can start this way, minimally, and grow new structure only as necessary. This significantly reduces the number of generations necessary to find a solution.

### Conclusion
NEAT is a powerful evolutionary algorithm that allows for the evolution of ANNs with the ability to grow and change their structure over time. By protecting innovation through speciation and minimizing dimensionality, NEAT is able to efficiently search through a minimal number of weight dimensions to find a solution.