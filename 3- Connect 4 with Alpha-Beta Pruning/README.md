# Assignment 3

## Overview
This code contains the implementation of a "connect-4" bot.

## Important Features and Optimizations

- **Iterative Deepening Alpha-Beta Pruning:** The player utilizes Iterative Deepening Alpha-Beta Pruning to explore the game tree efficiently. This technique allows the player to search deeper progressively within a specified time limit.

- **Move Exploration Order Optimization:** The player prioritizes certain moves, particularly those towards the middle, based on a move exploration order optimization strategy. This optimization aims to enhance the efficiency of move selection during the search process.

- **Transposition Table:** The engine implements a Transposition Table as an optimization strategy. This table helps in avoiding redundant calculations by storing previously evaluated positions.

- **Heuristic Evaluation:** The player incorporates a heuristic evaluation function to assess the game state. This evaluation considers factors such as the number of connected pieces and potential winning configurations to estimate the desirability of a given state.

## Video Demo

A video demonstration showcasing the functionality and performance of the player implementation is available. Please refer to the following link to view the demo:

[![Connect 4 Demo](https://img.youtube.com/vi/LXoNMUytonM/maxresdefault.jpg)](https://youtu.be/LXoNMUytonM)

### Use Cases Demonstrated:

1. **With a Search Depth >= 1:**
   Yellow should win the game immediately by placing a piece on top of the yellow stack at column 1.

2. **With a Search Depth >= 2:**
   Yellow should block red from winning the game on the next turn by placing its piece on column 5. A depth 1 search will not necessarily place the piece here, since depth 1 only checks for immediate wins. Depth 2 checks opponent replies to your own moves.

3. **With a Search Depth >= 3:**
   Yellow should recognize that in 3 moves it should win the game no matter what red does, as long as it places a piece to continue its current line along the bottom row. No matter where red will place its piece, it cannot win. Yellow should place its piece in column 2 or 5. A shallower search will not be able to draw this same conclusion.

4. **With a Search Depth >= 4:**
   Yellow should recognize that in 4 moves it will lose the game if it does not immediately place a piece to either side of red's pieces on the bottom row. If both ends are left open, red can place a piece in column 2 and then win the game on its next move. A shallower search than 4 will not be able to see this conclusion.


## Additional Resources and References

- The implementation of certain optimizations is inspired by resources such as [blog.gamesolver.org](http://blog.gamesolver.org/), particularly articles by Pascal Pons.

