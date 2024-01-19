### Traveling Salesman Problem Solver using Evolutionary Algorithm

This repository contains Python code to solve the Traveling Salesman Problem (TSP) using an evolutionary algorithm. The TSP is a classic combinatorial optimization problem where the goal is to find the shortest possible route that visits a set of cities and returns to the original city. This code provides an implementation of the evolutionary algorithm to find an approximate solution to the TSP.

## Requirements

- Python 3.x
- xmltodict library (install using `pip install xmltodict`)
- numpy library (install using `pip install numpy`)
- matplotlib library (install using `pip install matplotlib`)

## Usage

1. **Setting up the Problem:**
   - Change the `file_name` variable to the XML file containing the city distances data.
   - Update the `num_of_edges` variable to the number of cities in the problem instance.

2. **Configuring Algorithm Parameters:**
   - Modify the `population_size` variable to set the number of individuals in the population.
   - Adjust the `tournament_size` variable to set the size of the tournament selection.
   - Set the `termination_criteria` variable to specify the number of generations the algorithm will run.

3. **Running the Algorithm:**
   - Execute the Python script to run the evolutionary algorithm. The algorithm will evolve solutions to the TSP over multiple generations.

4. **Visualizing Results:**
   - The code includes functionality to plot the convergence curve, showing how the best solution improves over generations.
   - In order for the correct results to be displayed change the file_name, num_ofOedges and only run the cells corresponding to the file_name. 
   - Additionally, the following tables/graphs can be derived:
     - **Diversity table for different population:** Provides a table of the percentage of diversity in the paths for a given population.
     - **Keeping one parameter constant graphs:**
       - **Population vs Cost:** Plot the cost (fitness) of the best solution found for different population sizes while keeping the tournament size and other parameters constant.
       - **Tournament Size vs Cost:** Plot the cost of the best solution found for different tournament sizes while keeping the population size and other parameters constant.
     - **Minimum Cost for Each Type of Crossover, Mutation and Replacement:** Display the minimum cost achieved for each type of crossover and mutation operation used in the algorithm.

## Algorithm Details

- **Population Initialization:** The algorithm initializes a population of random routes, where each route represents a possible solution to the TSP.

- **Selection:** Tournament selection is used to select parents for crossover. The individuals are selected randomly, and the fittest individuals have a higher chance of being selected.

- **Crossover:** One-point, two-point and inversion crossover is implemented, creating offspring by combining parts of the parents' routes.

- **Mutation:** Single swap and multi swap mutation is applied to introduce genetic diversity in the population. It swaps the positions of two cities in an individual's route.

- **Replacement:** The worst individuals and random individuals in the population are replaced by the offspring, ensuring the population evolves towards better solutions.

## Graphs and Visualization

The code includes functionality to plot various graphs to visualize the algorithm's performance and behavior:
- **Convergence Curve:** Represents the best fitness (shortest route) found in the population at each generation, showing how the algorithm converges over time.
- **Diversity table for different population:** Displays the percentage of diversity in path for different population sizes.
- **Tournament Size vs Cost:** Plots the cost of the best solution found for different tournament sizes while keeping other parameters constant.
- **Minimum Cost for Each Type of Crossover, Mutation and Replacement:** Shows the minimum cost achieved for each type of crossover and mutation operation used in the algorithm.

