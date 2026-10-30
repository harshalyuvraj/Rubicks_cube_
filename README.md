# Rubik's Cube Solver

A C++ implementation of a Rubik's Cube solver featuring multiple cube representations, search algorithms, and pattern database-based heuristics.

## Features

- **Multiple Cube Representations:** Supports 1D array, 3D array, and bitboard representations.
- **Search Algorithms:** Implements BFS, DFS, Iterative Deepening DFS (IDDFS), and IDA*.
- **Pattern Databases:** Implements pattern database generation and lookup for heuristic-based search.
- **Modular Architecture:** Separates cube representations, solving algorithms, and pattern database components.

## Project Structure

```text
Rubicks_cube/
│
├── Databases/
│   └── cornerDepth5V1.txt
│
├── Model/
│   ├── PatternDatabase/
│   │   └── PatternDatabase.h
│   ├── RubiksCube.cpp
│   ├── RubiksCube.h
│   ├── RubiksCube1dArray.cpp
│   ├── RubiksCube3dArray.cpp
│   └── RubiksCubeBitboard.cpp
│
├── PatternDatabases/
│   ├── CornerDBMaker.cpp
│   ├── CornerDBMaker.h
│   ├── CornerPatternDatabase.cpp
│   ├── CornerPatternDatabase.h
│   ├── NibbleArray.cpp
│   ├── NibbleArray.h
│   ├── PatternDatabase.cpp
│   ├── PatternDatabase.h
│   ├── PermutationIndexer.h
│   ├── math.cpp
│   └── math.h
│
├── Solver/
│   ├── BFSSolver.h
│   ├── DFSSolver.h
│   ├── IDAstarSolver.h
│   └── IDDFSSolver.h
│
├── CMakeLists.txt
├── main.cpp
└── README.md
```

## Technologies Used

- C++14
- CMake 3.20+
- Standard Template Library (STL)

## Build and Run

### Prerequisites

- C++ compiler with C++14 support
- CMake 3.20 or later

### Build

```bash
cmake -S . -B build
cmake --build build
```

### Run

On Windows:

```bash
.\build\Debug\rubiks_cube_solver.exe
```

The executable location may vary depending on the compiler and build configuration.

## Implemented Algorithms

| Algorithm | Description |
|---|---|
| BFS | Breadth-First Search |
| DFS | Depth-First Search |
| IDDFS | Iterative Deepening Depth-First Search |
| IDA* | Iterative Deepening A* Search |

