# Coin Toss Experiment
## Overview

This Python program simulates a coin toss experiment where the goal is to determine how many tosses it takes to observe three heads. The experiment is repeated 1,000 times, and the program calculates and visualizes the average number of tosses required to observe three heads after each experiment.

### Key Features
- Simulate coin tosses until three heads are observed.
- Perform the experiment 1,000 times.
- Track and plot the average number of tosses required to get three heads after each experiment.
- The plot displays the trend over time with a focus on every 10th experiment.

## Requirements

Before running the program, make sure to install the required libraries:

- `random`: Built-in Python library to simulate randomness (no installation required).
- `matplotlib`: Python library for plotting graphs. Install it using pip:

```bash
pip install matplotlib
```

## Usage

1. **Initialization**: 
   - The `CoinTossExperiment` class is initialized with two parameters:
     - `target_heads`: The number of heads to observe (default is 3).
     - `num_experiments`: The number of experiments to perform (default is 1000).
   
2. **Main Flow**:
   - The `perform_experiment` method conducts the simulation of tossing a coin until three heads are observed in each of the 1,000 experiments.
   - After each experiment, the average number of tosses is updated and stored.
   
3. **Plotting**:
   - The `plot_experiment_results` method generates a plot where the x-axis represents the experiment number, and the y-axis represents the average number of tosses to get three heads.
   - The plot highlights every 10th experiment for clarity.

## Code Walkthrough

1. **CoinTossExperiment Class**:
   - **`__init__`**: Initializes the class with default values for the target number of heads and the number of experiments.
   - **`toss_until_target_heads`**: Simulates a coin toss until the target number of heads is reached. It uses `random.choice(['H', 'T'])` to simulate heads (`H`) or tails (`T`).
   - **`perform_experiment`**: Runs the experiment for the specified number of times and tracks the total tosses.
   - **`plot_experiment_results`**: Uses `matplotlib` to plot the average number of tosses required after each experiment.

2. **Main Block**:
   - Creates an instance of `CoinTossExperiment` and runs the experiment.
   - The result is displayed as a graph showing the average tosses required to get three heads.

## Example Usage

```python
if __name__ == "__main__":
    # Create an instance of CoinTossExperiment with 3 heads and 1000 experiments
    experiment = CoinTossExperiment(target_heads=3, num_experiments=1000)
    experiment.perform_experiment()  # Perform the experiment
    experiment.plot_experiment_results()  # Plot the results
```

This will simulate 1,000 coin toss experiments, calculate the average number of tosses required to get three heads, and display a graph showing how the average number of tosses evolves over the course of the experiments.

## Output

The program will generate a graph with:
- **X-axis**: The number of experiments.
- **Y-axis**: The average number of tosses required to get 3 heads.

The graph helps in visualizing the trend in the average number of tosses across the 1,000 experiments.

![Output1](https://github.com/AartiDashore/CoinTossExperiment/blob/main/Output1.png)

## Customization

- You can modify the number of heads needed by changing the `target_heads` parameter when initializing the `CoinTossExperiment`.
- You can adjust the number of experiments by changing the `num_experiments` parameter.

For example:

```python
experiment = CoinTossExperiment(target_heads=5, num_experiments=500)
```

This would simulate the experiment to observe 5 heads, and repeat it 500 times instead of 1,000.

## Conclusion

This program provides a simple but effective simulation of repeated coin tosses to study how many tosses it takes to observe a set number of heads. The visualization allows you to understand the behavior and trends that emerge from the repeated trials.
