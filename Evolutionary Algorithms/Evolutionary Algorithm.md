---
description: An introduction to Evolutionary Algorithms (EAs), including their theoretical background, implementation, types, constraints, exploitative-exploratory search, execution environment, modularity, system scale, and applications.
---
# Evolutionary Algorithms

## Introduction
Evolutionary Algorithms (EAs) are a type of optimization algorithm inspired by biological evolution. They are used to solve complex problems by mimicking the process of natural selection and genetic recombination.

## Overview
An evolutionary algorithm (EA) is a population-based metaheuristic optimization algorithm that uses mechanisms inspired by biological evolution, such as reproduction, mutation, recombination, and selection. Candidate solutions to the optimization problem play the role of individuals in a population, and the fitness function determines the quality of the solutions. Evolution of the population then takes place after the repeated application of the above operators.

## Theoretical Background
Evolutionary algorithms often perform well approximating solutions to all types of problems because they ideally do not make any assumption about the underlying fitness landscape. Techniques from evolutionary algorithms applied to the modeling of biological evolution are generally limited to explorations of microevolutionary processes and planning models based upon cellular processes.

## Implementation
The following is an example of a generic single-objective genetic algorithm:
1. Generate the initial population of individuals randomly. (First generation)
2. Repeat the following regenerational steps until termination:
   1. Evaluate the fitness of each individual in the population (time limit, sufficient fitness achieved, etc.)
   2. Select the fittest individuals for reproduction. (Parents)
   3. Breed new individuals through crossover and mutation operations to give birth to offspring.
   4. Replace the least-fit individuals of the population with new individuals.

## Types
- Evolutionary programming
- Genetic algorithm
- Differential evolution
- Coevolutionary algorithm
- Genetic programming

## Constraints
- Constraints are the physical goals that represent the real-world limitations of a problem.
- They take a theoretical problem and make it realistic.
- Constraints are the limitations imposed on the entities, such as code size, energy consumption, or execution time.

## Exploitative-Exploratory Search
- EAs use recombination and mutation for exploitative and exploratory search.
- The more mutation that occurs, the more exploratory the search, and correspondingly, the less mutation, the more exploitative the search.
- EAs can be at either end of the spectrum, with only recombination (more exploitative) or only mutation (more exploratory).
- The ratios of recombination and mutation can be fixed or dynamic.

## Execution Environment, Modularity, and System Scale
- EAs can execute as a process within an Operating System, as a self-constructed dynamic program feed into a language interpreter, or within a simulator.
- To handle larger problems, some form of modularity has to be adopted.
- EAs can scale from one process to many processes running on several server clusters.
- These compute clusters are called islands and operate in either a parallel and/or distributed fashion.

## Applications
Evolutionary algorithms are often used in optimization problems, including numerical optimization and combinatorial tasks. They can also be used in genetic improvement, schema, Eurisko, and parity benchmark.