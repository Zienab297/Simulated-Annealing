# Simulated Annealing

This repository contains a Jupyter Notebook implementing the **Simulated Annealing** algorithm, a probabilistic technique for solving optimization problems. Simulated Annealing is particularly useful for finding an approximate solution to complex problems with a large search space where traditional methods may be inefficient.

## Overview
The notebook demonstrates how Simulated Annealing can solve an optimization problem. The implementation includes customizable parameters for temperature, cooling schedules, and acceptance criteria. The annealing process inspires this metallurgy technique and mimics metal cooling to reach a low-energy crystalline state.

## Features
- Customizable parameters for:
  - Initial temperature
  - Cooling rate
  - Iterations per temperature step
- Visualization of the optimization process
- Simple interface for defining custom optimization problems
- Example problem setup included in the notebook

## Simulated Annealing Algorithm
The Simulated Annealing algorithm is inspired by the process of annealing in metallurgy. It involves the following steps:

1. Initialize the system with a random solution and a high temperature.
2. Repeat until the system is sufficiently cooled:
   - Generate a neighboring solution by modifying the current solution.
   - Calculate the change in the objective function (∆E).
   - If the new solution improves the objective function (∆E < 0), accept it.
   - If the new solution worsens the objective function, accept it with a probability proportional to the temperature. This probability is calculated as $`\exp(\frac{-\Delta E}{T})`$, where $` \Delta E `$ is the change in the objective function and $` T `$ is the current temperature. For example, if $` \Delta E = 5 `$ and $`T = 100`$, the acceptance probability is approximately 0.95.
   - Gradually reduce the temperature using a cooling schedule.
3. Return the best solution found.

## Results
The notebook visualizes the progress of the algorithm, showing how the solution evolves over time as the temperature decreases. The visualizations are static plots generated at the end of the optimization process, allowing users to analyze the results after execution. The example included demonstrates the algorithm's ability to converge to a near-optimal solution for the given optimization problem.
