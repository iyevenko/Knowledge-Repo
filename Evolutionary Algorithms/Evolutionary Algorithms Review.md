---
description: A review of the IEEE paper "Degree of population diversity X Optimized Collision Free" which proposes a new taxonomy of evolutionary algorithms and discusses the need for their integration into society while conforming to regulatory rules.
---
# Evolutionary Algorithms Review

## Introduction
The IEEE Degree of population diversity X Optimized Collision Free paper (1906.08870.pdf) is currently open on the screen. It discusses evolutionary algorithms and their increasing use and development due to the availability of computation and open source software libraries.

## Taxonomy of Evolutionary Algorithms
The paper proposes a new taxonomy of evolutionary algorithms based on five main areas:
- Managing control of the environment with limiters
- Explaining and repeating the search process
- Understanding input and output causality within a solution
- Managing algorithm bias due to data or user design
- Adding corrective measures

## Classification of Algorithms
The paper briefly classifies a broad range of algorithms and identifies areas of future research.

## Evolutionary Algorithms

Evolutionary algorithms (EAs) are a type of optimization algorithm that are inspired by biological evolution. The basic digital process adopted by many EAs is shown in Figure 3.2.

### Population

A population is a set of solution candidates or entities. Each population is created temporally and has the potential to age with each evolutionary cycle (generation). The initial population is either seeded randomly or is sampled from a set of known solutions.

There are two ways for the population to be evolved: 

1. Evolving the entire population to create the next generation.
2. Evolving individual entities within the population (called Steady-State). 

Entities can die or thrive between generations.

The size of the population can be fixed or dynamic throughout the evolutionary process. Fixed is when the number of entities is kept constant and dynamic is when the population size changes. If dynamic, a larger initial population may bring some potential advantages. This is especially true when choosing the first strong candidates for further evolution.

A population can also be divided into subgroups, these subgroups are called demes. A deme is a biological term that describes a group of evolving organisms with the same taxonomy. They can evolve isolation within the population. Demes can be made to interact with the other demes. This is often described using an island and canoe metaphor, where the demes are the islands and the interactions occur as canoes move between the islands depositing new entities.

## Conclusion
The review highlights the need for evolutionary algorithms to integrate into society and human processes, conforming to societal concerns and government regulatory rules.