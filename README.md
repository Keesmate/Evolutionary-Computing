# Generalist Agent in the EvoMan Framework: A NeuroEvolutionary Comparison
# Project Summary
This project was a collaborative effort to compare two neuroevolutionary techniques for training a generalist agent in the EvoMan framework during the Evolutionary Computing course at the Vrije Universiteit, Amsterdam. The EvoMan framework is a video game environment where a single agent is tasked with defeating eight distinct enemies. We used a neural network to control the agent, with game state sensors as inputs and the agent's actions as outputs. 
The main goal was to see which algorithm could evolve an agent that would generalize better to enemies it had not seen during training.
My specific contributions to this project included the development and implementation of the algorithms and hyperparameter tuning.
A comprehensive report detailing the methodology, results, and discussion can be found in the repository in the ["Report"](/Report) folder.

# Research Question
The central question of this project was to determine if the ability to evolve a neural network's topology, as seen in the NeuroEvolution of Augmenting Topologies (NEAT) algorithm, would lead to better generalizable performance against unseen enemies compared to a fixed-topology Genetic Algorithm (GA) approach.

# Data
The project did not use a traditional dataset. Instead, the "data" was the game state of the EvoMan framework, which provided sensor readings to the neural network controlling the agent. This included information about the agent's and enemy's health, position, and other game variables.

# Methodology
1. Algorithm Implementation
   - Fixed-Topology Genetic Algorithm (GA): A GA was implemented to evolve only the weights of a fixed-topology, fully-connected neural network. This served as a benchmark for comparison.
   - NeuroEvolution of Augmenting Topologies (NEAT): We used the NEAT Python library to implement a neuroevolutionary approach that could evolve both the weights and the structure of the neural network.

2. Training and Evaluation
   - Both algorithms were trained on two different groups of three enemies over 30 generations.
   - The trained agents were then tested against all eight enemies to evaluate their generalization capabilities.
   - We performed hyperparameter tuning with Optuna to find the optimal settings for both algorithms.

3. Fitness Function
   - The performance of each agent was measured using a fitness function that considered both the agent's remaining health and the damage inflicted on the enemy.

# Key Findings and Conclusions
Contrary to our initial hypothesis, the fixed-topology Genetic Algorithm (GA) demonstrated a better ability to generalize to new enemies compared to the more complex NEAT algorithm. A potential reason for this unexpected outcome was a bias in our experimental setup: the training enemy groups were selected based on preliminary testing with the GA, which may have given it an unfair advantage.
This project highlights the challenges in designing unbiased comparative studies for evolutionary algorithms. It suggests that a simpler, fixed-topology approach can sometimes outperform more complex, dynamically evolving algorithms in a generalist setting, and that the methodology for selecting training environments is a critical factor in the outcome of such studies.

# Authors
Tomasz Kubrak

Rafal Kukielka

Kieran Keesmaat

Jan Kaleta-Slyk
