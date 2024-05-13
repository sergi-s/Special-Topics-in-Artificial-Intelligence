# COMP6980 - Assignment 2

## Overview
This code implements the A* algorithm for pathfinding, with support for both unidirectional and bidirectional search modes. It includes multiple heuristic options such as 8-directional Manhattan, 4-directional Manhattan, and 2D Euclidean distance. 

## Implementation
The implementation consists of a class `Search_Student` which represents the search algorithm. Here's a brief overview of important methods:

- **canFit(x, y, size)**: Computes whether a given size agent can fit at the specified (x, y) location.
- **computeSectors()**: Computes sectors using 4D BFS algorithm.
- **isConnected(x1, y1, x2, y2, size)**: Determines whether two locations are connected.
- **isLegalAction(x, y, action)**: Computes whether the given action can be performed from the given position.
- **estimateCost(x, y, gx, gy)**: Computes the heuristic function h(n) from start location to goal location.
- **startSearch(sx, sy, gx, gy, size)**: Initiates the search algorithm.
- **searchIteration()**: Performs a single iteration of the search algorithm.
- **getOpen()**: Returns the current open list states.
- **getClosed()**: Returns the current closed list states.

## Unidirectional vs Bidirectional Search
- **Unidirectional Search**: Searches from the start node towards the goal node.
- **Bidirectional Search**: Searches from both the start and goal nodes simultaneously, meeting at some midpoint.

## Heuristic Options
- **8-directional Manhattan**: Considers all 8 possible movement directions.
- **4-directional Manhattan**: Considers only the 4 cardinal directions.
- **2D Euclidean Distance**: Computes straight-line distance between two points.

## Admissibility of Heuristics
- **8-directional Search with 4-directional Heuristic**: Not admissible because it underestimates the true cost, leading to suboptimal paths.

#### Video: Searches with different options
[![BFS Algorithm](https://img.youtube.com/vi/DajZy4A2tA8/maxresdefault.jpg)](https://youtu.be/DajZy4A2tA8)
