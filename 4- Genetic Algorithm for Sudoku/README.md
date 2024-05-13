# Genetic Algorithm for Sudoku

This code implements a genetic algorithm (GA) to solve Sudoku puzzles. Here's a brief overview of the key components:

- **Genetic Evolution Function:** The `GAEvolve` function drives the genetic evolution process. It selects parents based on fitness using roulette wheel selection, performs crossover, mutation, and generates the next population.

- **Crossover Techniques:** Two main crossover techniques are implemented:
  - **Subgrid Crossover:** A subgrid from one parent is combined with the rest from another parent.
  - **Row-Column Crossover:** Rows or columns from one parent are selected based on a random index, and the rest from another parent.

- **Fitness Functions:**
  - **Sudoku Fitness:** Evaluates the fitness of a Sudoku solution based on the uniqueness of values in rows, columns, and squares, penalizing conflicts and empty squares.
  - **Sum Values Fitness:** Computes the fitness of a solution based on the sum of values in each row, column, and diagonal.
  - **Match Row Fitness:** Calculates the fitness by comparing each row's values with a target row.
  - **Match Column Fitness:** Calculates the fitness by comparing each column's values with a target column.
  - **Checker Fitness:** Checks for the presence of specific values in the Sudoku solution, rewarding matches and penalizing deviations.

- **Parameter Optimization:** Adjusting certain parameters can affect the performance of the genetic algorithm:
  - **Increased Population Size:** Larger populations can increase diversity and exploration but may require more computational resources.
  - **Increased % Individuals Mutated:** Higher mutation rates introduce more randomness, potentially exploring new solutions but risking convergence to local optima.
  - **Increased % Random Genes Inserted:** Inserting more random genes can enhance diversity but may slow down convergence if too many solutions are discarded.
  - **Increased % Elite Genes Survive:** More elite genes surviving from one generation to the next can help preserve promising solutions but may limit exploration.

This genetic algorithm offers a novel approach to solving Sudoku puzzles by mimicking the process of natural selection and evolution. For detailed implementation and usage instructions, please refer to the code comments and documentation within the `GA_Student.js` file.

## Demo Video

For a visual demonstration of the genetic algorithm solving Sudoku puzzles, please check out the accompanying demo video.

[![Genetic Algorithm for Sudoku](https://img.youtube.com/vi/lh_ZdV_rNrI/maxresdefault.jpg)](https://youtu.be/lh_ZdV_rNrI)
