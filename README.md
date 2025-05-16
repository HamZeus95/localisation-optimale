# Optimization Algorithms Comparison

This project compares four popular optimization algorithms:
1. **Genetic Algorithm (GA)**
2. **Simulated Annealing (SA)**
3. **Tabu Search**
4. **Particle Swarm Optimization (PSO)**

The algorithms are compared on a Traveling Salesman Problem (TSP) using city data from `data.csv`.

## Problem Description

The optimization problem is to find the shortest possible route that visits the 20 most populated cities in the world and returns to the starting city (a classic Traveling Salesman Problem).

## Algorithms Overview

### Genetic Algorithm (GA)
- Based on natural selection and genetic operations
- Uses crossover, mutation, and selection to evolve better solutions
- Generally provides high-quality solutions but is computationally intensive
- **Time Complexity**: O(generations * pop_size² * n)
- **Space Complexity**: O(pop_size * n)

### Simulated Annealing (SA)
- Inspired by the annealing process in metallurgy
- Gradually reduces the probability of accepting worse solutions
- Balances exploration and exploitation
- Usually fast with good quality solutions
- **Time Complexity**: O(iterations * n)
- **Space Complexity**: O(n)

### Tabu Search
- Uses memory structures (tabu lists) to avoid revisiting recent solutions
- Effective at escaping local optima
- Good at finding high-quality solutions in complex search spaces
- **Time Complexity**: O(iterations * n²)
- **Space Complexity**: O(tabu_size + n²)

### Particle Swarm Optimization (PSO)
- Inspired by social behavior of bird flocking or fish schooling
- Each particle moves based on its own experience and the global best
- Effective for continuous optimization problems but adapted here for TSP
- **Time Complexity**: O(iterations * num_particles * n)
- **Space Complexity**: O(num_particles * n)

## Files

- `compare.py` - Main Python script that implements and compares the algorithms
- `data.csv` - Dataset containing city information (name, coordinates, population, etc.)
- `convergence_comparison.png` - Graph showing how each algorithm converges over iterations
- `performance_comparison.png` - Bar charts comparing final distance and execution time
- `route_comparison.png` - Visual representation of the routes found by each algorithm
- `algorithm_comparison.csv` - CSV file with detailed performance metrics

## How to Run

1. Ensure you have Python installed with the required packages:
   ```
   pip install pandas numpy matplotlib seaborn tqdm
   ```

2. Run the comparison script:
   ```
   python compare.py
   ```

3. The script will:
   - Load the city data from `data.csv`
   - Run each of the four algorithms
   - Generate visualizations for comparison
   - Save the results in various output files

## Results Interpretation

The comparison is based on:
1. **Solution Quality** - The total distance of the tour (lower is better)
2. **Execution Time** - How long the algorithm takes to run (faster is better)
3. **Convergence Speed** - How quickly the algorithm approaches the final solution

The visualization files help understand the trade-offs between these factors for each algorithm.

## Customization

You can modify parameters in the `compare.py` file to:
- Change the number of cities to include in the TSP
- Adjust algorithm-specific parameters (generations, cooling rate, etc.)
- Modify visualization settings
- Change the weights used in the overall score calculation

## Dependencies

- pandas - For data handling
- numpy - For numerical operations
- matplotlib - For basic visualization
- seaborn - For enhanced visualization
- tqdm - For progress bars

## License

This project is provided for educational purposes.

## Credits

The city dataset is from SimpleMaps World Cities Database.
