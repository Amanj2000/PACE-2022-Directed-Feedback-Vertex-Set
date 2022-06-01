# FEDRER - Feedback vertex set using Edge Density and REmove Redundant

This repository contains a heuristic solution to the Directed Feedback Vertex Set problem.

The program is submitted to the [PACE Challenge 2022](https://pacechallenge.org/2022/).

The **Directed Feedback Vertex Set** Problem is defined as follows:

**Input**: A directed graph $G = (V, E)$

**Output**: Find a minimum subset $X \subseteq V$ such that, when all vertices of $X$ and their adjacent edges are deleted from $G$, the remainder is acyclic

Thus, a feedback vertex set of a graph is a set of vertices whose deletion leaves a graph **acyclic**.

## Requirements

-   A 64-bit Linux operating system.
-   A modern, ![C++17](https://img.shields.io/badge/C++-17-blue.svg?style=flat)-ready compiler
-   The [cmake][cmake] build system (>= 3.16).

## Build Application

1. Clone the repository:

    `git clone git@github.com:Amanj2000/PACE-2022-MFVS.git`

2. Run cmake: `cmake .`
3. Run make: `make`
4. A static code binary named `fedrer` will now be available in the root directory

## Run Application

The program reads a directed graph instance from stdin and print the FVS to stdout.
For the input and output format, please refer the [PACE challenge - Heuristic Track](https://pacechallenge.org/2022/tracks/#heuristic-track) page.

A usage example would be:

    cat input_graph | ./fedrer > fvs.txt

By default, the solver runs till it receives a `SIGTERM`.

## Submit

Prepare CMake submission for optil.io with

    tar -czvf fedrer.tgz fedrer.cpp CMakeLists.txt

[cmake]: http://www.cmake.org/ "CMake tool"
