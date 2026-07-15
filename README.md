# Evolutionary Algorithm for the Traveling Salesman Problem

This repository contains a Jupyter notebook that implements an evolutionary algorithm for the Traveling Salesman Problem (TSP) using an **indirect approach**.

Instead of representing a solution directly as a tour permutation, the algorithm evolves a Grefenstette integer genotype. A decoder then converts each genotype into a valid TSP tour. This guarantees that every decoded solution visits each city exactly once, while still allowing simple evolutionary operators such as one-point crossover and random-reset mutation.

## Approach

This notebook uses an **indirect representation**:

Grefenstette genotype -> decoder -> valid TSP tour -> tour distance

A direct approach would store the tour itself as a permutation. However, standard crossover operators can easily create invalid tours with repeated or missing cities. The indirect approach avoids this by evolving a genotype that is decoded into a feasible tour.

## Features

- Implements a Grefenstette decoder for TSP tours.
- Uses an indirect genotype-to-phenotype representation.
- Applies binary tournament selection.
- Uses one-point crossover and random-reset mutation.
- Includes elitism to preserve the best solution.
- Evaluates performance on official TSPLIB95 benchmark instances:
  - berlin52
  - st70
  - eil101
- Compares results against known optimal tour lengths.
- Reports best distance, average distance, fitness, relative gap, and runtime.
- Plots convergence curves and the best tour found for each instance.

## Technologies

- Python
- NumPy
- pandas
- matplotlib
- Jupyter Notebook

## Purpose

This notebook is intended as an educational implementation of evolutionary optimization for the Traveling Salesman Problem. It demonstrates how an indirect representation can preserve feasibility in permutation-based problems and provides a benchmark-based evaluation using standard TSPLIB95 instances.
