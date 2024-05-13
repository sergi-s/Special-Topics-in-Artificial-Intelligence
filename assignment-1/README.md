## 1. Class Structure

The algorithm is encapsulated within the `Search_Student` class, designed to handle the search process. It contains essential properties and methods for initializing, starting, and iterating through the search.

## 2. Initialization

- **Constructor:**
  - Initializes the search configuration, grid, start and goal positions, cost, and other necessary variables.
  
## 3. Start Search

- **startSearch(sx, sy, gx, gy):**
  - Initiates the search process by setting the start and goal positions.
  - Resets open and closed lists and creates the root node representing the start state.
  - Marks the search as in progress.

## 4. Search Iteration

- **searchIteration():**
  - Performs one iteration of the search process.
  - Expands nodes based on the selected search strategy (BFS or DFS).
  - Checks for the goal state, updates path, and sets the cost if the goal is found.
  - Manages open and closed lists to keep track of visited nodes.
  
## 5. Node Expansion

- **expand(node):**
  - Expands a given node by generating child nodes based on legal actions.
  - Child nodes are added to the open list for future exploration.

## 6. Iterative Deepening Depth-First Search (IDDFS)

- **searchIterationIDDFS():**
  - Handles search iterations specifically for Iterative Deepening Depth-First Search.
  - Increments the search depth with each iteration.
  - Expands nodes only if their depth is within the current depth limit.
  - Manages cutoff conditions when the depth limit is reached.

## 7. Legal Actions and State Checking

- **isLegalAction(x, y, action):**
  - Checks if a given action is legal from a specified position on the grid.
  - Ensures that the new state is within the grid boundaries and maintains consistency with the grid values.

## 8. Result and Path Construction

- **foundGoal(node):**
  - Constructs the path when the goal state is found.
  - Sets the cost based on the length of the path.
  
- **didNotFindGoal():**
  - Handles situations where the goal state is not found.
  - Marks the search as not in progress, resets variables, and sets the cost to -1.

## 9. CloseList Optimization

- **CloseList class:**
  - Implements a 2D array for optimizing the tracking of visited points.
  - Saves and looks up points efficiently.
  - Allows resetting and retrieving all points.

## 10. Usage and Configuration

- **Usage section in README:**
  - Provides instructions on how to use the algorithm.
  - Explains the configuration options, including legal actions, action costs, and search strategy.

## 11. Media Section

### Breadth-First Search (BFS)

#### Image: BFS Visualization
![BFS Visualization](/COMP6980_A1_srizkallah/media/BFS.png)

#### Video: BFS Algorithm in Action
[![BFS Algorithm](/COMP6980_A1_srizkallah//media/BFS.png)](https://youtu.be/RkOh7328P44)



### Depth-First Search (DFS)

#### Image: DFS Visualization
![DFS Visualization](/COMP6980_A1_srizkallah//media/DFS.png)

#### Video: DFS Algorithm in Action
[![DFS Algorithm](/COMP6980_A1_srizkallah//media/DFS.png)](https://youtu.be/a4rH3vMH-LA)


### Iterative Deepening Depth-First Search (ID-DFS)

#### Image: ID-DFS Visualization
![ID-DFS Visualization](/COMP6980_A1_srizkallah//media/DFS.png)

#### Video: ID-DFS Algorithm in Action
[![ID-DFS Algorithm](/COMP6980_A1_srizkallah//media/ID-DFS.png)](https://youtu.be/GvyiwZuNRco)


These main ideas collectively form a basic framework for a grid-based search algorithm that can be applied to various problems. The specific search strategy (BFS, DFS, IDDFS) and the grid-related details are crucial aspects of the algorithm's functionality.

