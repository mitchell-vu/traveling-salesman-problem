# Design a Genetic Algorithm to solve TSP

## Overview

**Traveling salesman problem (TSP)** is a famous problem in Computer Science and may be familiar to you. The problem statement is simple, given a graph $G = (V, E)$ where $V$ is the set of nodes, $E$ is the set of edges, there is additional information about distances between nodes.

The goal of this problem is to output the shortest route starting from $V_{start}$ and ending at $V_{start}$, such that each node is visited once. In this project, you are asked to implement a **Genetic Algorithm (GA)** to determine the (near-)optimal route.

## Basic Knowledge

- Algorithm
- Data structure

_Note_: You don't need advanced knowledge about the evolutionary algorithm, you can deploy this project without any prior knowledge of GA

## Specifications

### Algorithm overview

In this project, you must implement a GA algorithm to solve TSP, your proposed method may be simple and you should not focus too much on advanced GA techniques. Here is a simple guide for deploying this algorithm to solve the TSP:

**Step 1** Design an encode-decode mechanism for each route

The simplest way is to use permutational encoding

For example, to represent a route `0 → 4 → 5 → 1 → 2 → 3 → 0`, we can use `(4, 5, 1, 2, 3)` or `(0, 4, 5, 1, 2, 3)`,...

We call this representation as **_chromosome_**

**Step 2:** Create a population with N individuals, each individual is a _chromosome_ of a route

For example, individual `A = (4, 5, 1, 2, 3)`

**Step 3:** Design a crossover mechanism

Given input as two individuals, output two offspring. You can refer to many mechanisms, one simple approach is one-point crossover, you can refer to it [here](<https://en.wikipedia.org/wiki/Crossover_(genetic_algorithm)>), and also many other sources.

**Step 4:** Design a mutation mechanism

There are many methods, one simplest way is to swap two genes in a _chromosome_

**Step 5:** Design a parent's selection and mutation implementation

**Step 6:** Repeat selecting parents and mutating to evolve the population

You can refer to a full-detail algorithm at [this video](https://www.youtube.com/watch?v=3GAfjE_ChRI)

### GUI

You can freely design your own GUI to demonstrate the found route. You can refer to these sources to have some ideas:

- [youtube.com/watch?v=94p5NUogClM](https://www.youtube.com/watch?v=94p5NUogClM)
- [youtube.com/watch?v=u_WHKDYHltE](https://www.youtube.com/watch?v=u_WHKDYHltE)

### Design

- On the main menu

  - [ ] Title of the application

  - [ ] 3 buttons for the sort algorithms for the user to help, solve the TSP, and quit:

    - [ ] Help menu shows the basic usage and aim of the program
    - [ ] Quit option exits the program. Remember to ask for confirmation

- In the demonstration:

  - [ ] A button for starting the simulation, namely, “Start”

  - [ ] A visualization for the individual that currently holds the best fitness, in array-structure

  - [ ] A visualization for the individual that currently holds the best fitness, in graph-structure

_Note_: If you use any Java implementations, you must design your wrapper to show your OOP design in the project.
