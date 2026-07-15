# Traveling-SalesMan-Problem
Evolutionary algorithm for the Traveling Salesman Problem using an indirect Grefenstette representation, tested on TSPLIB95 benchmark instances.

# Evolutionary Algorithm for the Traveling Salesman Problem

This repository contains a Jupyter notebook that implements an evolutionary algorithm for the Traveling Salesman Problem (TSP) using an **indirect approach**.

Instead of representing a solution directly as a tour permutation, the algorithm evolves a Grefenstette integer genotype. A decoder then converts each genotype into a valid TSP tour. This guarantees that every decoded solution visits each city exactly once, while still allowing simple evolutionary operators such as one-point crossover and random-reset mutation.

## Approach

This notebook uses an **indirect representation**:

```text
Grefenstette genotype -> decoder -> valid TSP tour -> tour distance
