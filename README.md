
# N-Queens Problem Solver using Genetic Algorithm

This repository contains an implementation of a Genetic Algorithm to solve the N-Queens problem. The algorithm finds a configuration of N queens on an NxN chessboard such that no two queens threaten each other.

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Code Structure](#code-structure)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview

The N-Queens problem is a classic AI problem where the goal is to place N queens on an NxN chessboard so that no two queens can attack each other. This implementation uses a Genetic Algorithm to find a solution by evolving a population of potential solutions over several generations.

Key components of the project:
- Random chromosome generation
- Fitness calculation
- Crossover and mutation
- Roulette-wheel selection
- Genetic algorithm to evolve the population

## Installation

To run the code, you need to have Python installed. No additional libraries are required as the implementation relies on standard Python libraries.

## Usage

1. Clone the repository:
    ```bash
    git clone https://github.com/your_username/n-queens-genetic-algorithm.git
    cd n-queens-genetic-algorithm
    ```

2. Run the script:
    ```bash
    python n_queens_ga.py
    ```

3. Enter the desired number of queens when prompted.

## Code Structure

- `random_chromosome(size)`: Generates a random chromosome representing a potential solution.
- `fitness(chromosome, maxFitness)`: Calculates the fitness of a chromosome based on the number of non-attacking pairs of queens.
- `crossover(x, y)`: Performs crossover between two chromosomes to produce a child chromosome.
- `mutate(x)`: Mutates a chromosome by randomly changing the value of a gene.
- `probability(chromosome, maxFitness)`: Calculates the probability of selecting a chromosome based on its fitness.
- `random_pick(population, probabilities)`: Selects a chromosome from the population based on roulette-wheel selection.
- `genetic_queen(population, maxFitness)`: Runs the genetic algorithm to evolve the population towards a solution.
- `print_chromosome(chrom, maxFitness)`: Prints a chromosome and its fitness.
- `print_board(chrom)`: Prints the chessboard representation of a chromosome.

### Key Functions and Methods:

- `random_chromosome(size)`: Generates a random solution.
- `fitness(chromosome, maxFitness)`: Evaluates the fitness of a solution.
- `crossover(x, y)`: Combines two solutions to create a new one.
- `mutate(x)`: Introduces genetic diversity by mutating a solution.
- `random_pick(population, probabilities)`: Selects solutions for the next generation based on their fitness.
- `genetic_queen(population, maxFitness)`: Evolves the population to find an optimal solution.
- `print_chromosome(chrom, maxFitness)`: Displays a solution and its fitness.
- `print_board(chrom)`: Visualizes a solution on a chessboard.

## Results

The algorithm iteratively evolves a population of solutions, selecting the best solutions to produce offspring. Over successive generations, the population converges towards an optimal solution.

### Example Output:

- **Generation Output:**
  ```
  === Generation 10 ===
  Maximum Fitness = 28
  ```

- **Solution Output:**
  ```
  Chromosome = [0, 4, 7, 5, 2, 6, 1, 3],  Fitness = 28

  Q x x x x x x x
  x x x x Q x x x
  x x x x x x x Q
  x x x x x Q x x
  x x Q x x x x x
  x x x x x x Q x
  x Q x x x x x x
  x x x Q x x x x
  ```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
