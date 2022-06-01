# FEDRER - Feedback vertex set using Edge Density and REmove Redundant

This repository contains a heuristic solution to the Directed Feedback Vertex Set problem.

The program is submitted to the [PACE Challenge 2022](https://pacechallenge.org/2022/).

The feedback vertex set problem (FVSP) consists in making a given directed
graph acyclic by removing as few vertices as possible.

## Requirements

-   A 64-bit Linux operating system.
-   A modern, ![C++17](https://img.shields.io/badge/C++-17-blue.svg?style=flat)-ready compiler
-   The [cmake][cmake] build system (>= 3.16).

## Build Application

1. Clone the repository:

    `git clone git@github.com:Amanj2000/PACE-2022-MFVS.git`

2. Run cmake: `cmake .`
3. Run make: `make -j 8`

## Run Application

The program reads a directed graph instance from stdin and print the FVS to stdout.
For the input and output format, please refer to the [PACE challenge web page](https://pacechallenge.org/2022/).

A usage example would be:

    cat input_graph | ./fedrer > fvs.txt

By default, the solver runs till it receives a SIGTERM.

## Submit

Prepare CMake submission for optil.io with

    tar -czvf fedrer.tgz fedrer.cpp CMakeLists.txt

[cmake]: http://www.cmake.org/ "CMake tool"
