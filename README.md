# Flappy-Bird-Genetic-Algorithm---NEAT

![image](https://github.com/user-attachments/assets/11ce922d-276c-457c-ad88-4365f42edfae)


# **Flappy Bird with NEAT (NeuroEvolution of Augmenting Topologies)**

This project demonstrates the use of a genetic algorithm to train an artificial intelligence (AI) to play the classic Flappy Bird game. The AI is developed using the **NEAT algorithm** (NeuroEvolution of Augmenting Topologies), which evolves neural networks to optimize their performance over generations.

---

## **Table of Contents**

1. [Overview](#overview)  
2. [Features](#features)  
3. [How It Works](#how-it-works)  
4. [Requirements](#requirements)  
5. [Setup](#setup)  
6. [Usage](#usage)  
7. [Demo](#demo)  
8. [Future Work](#future-work)  
9. [References](#references)

---

## **Overview**

In this project, multiple neural networks are created to control a virtual bird in the Flappy Bird game. These networks are evaluated based on their ability to keep the bird alive. Over successive generations, the neural networks evolve to become better at playing the game using **NEAT**, a genetic algorithm for evolving neural networks.

**Key Objectives:**
- Simulate Flappy Bird gameplay using AI agents.
- Train the agents using a genetic algorithm (NEAT).
- Observe the evolution of AI agents over generations.

---

## **Features**

- **NEAT Algorithm**: A genetic algorithm that evolves neural networks by adjusting topology and weights.
- **Flappy Bird Simulation**: A Python-based simulation of the Flappy Bird game.
- **Performance Tracking**: Evaluate AI agents based on fitness (survival time and score).
- **Dynamic Evolution**: Neural networks improve across generations by mutating weights and structures.

---

## **How It Works**

1. **Neural Network Creation**:
   - Each bird is controlled by a neural network.
   - Input features include the bird's position, the distance to the next pipe, and the gap's height.

2. **Fitness Function**:
   - Birds are scored based on how far they progress (time alive + pipes cleared).

3. **Evolution Process**:
   - After each generation:
     - The top-performing birds (neural networks) are selected.
     - Crossover and mutation are applied to create the next generation.
     - Poor-performing birds are discarded.

4. **Training Iterations**:
   - The process continues until the neural networks are able to achieve high scores consistently.

---

## **Requirements**

- Python 3.7+
- Libraries:
  - `pygame`
  - `neat-python`
  - `numpy`
  - `matplotlib`

Install the required libraries using:
```bash
pip install -r requirements.txt

```

---

## **Setup**

1. **Clone the Repository**:

   Clone this repository to your local machine:
   ```bash
   git clone https://github.com/username/flappy-bird-neat.git
   cd flappy-bird-neat
   ```
2. **Install Dependencies**:

   Install the required Python libraries using the following command:

  bash
  Copy code
  pip install -r requirements.txt
3. **Configure NEAT Parameters**: 
  
  The NEAT configuration file (config-feedforward.txt) allows you to modify hyperparameters such as:

  **Population size**: Number of birds per generation.
  
  **Mutation rates**: The probability of weight or topology changes.
  
  **Fitness threshold**: The score required to end training.
  
You can tweak these parameters to experiment with different setups and training behaviors.





---

---

## **Usage**

### **Run the Simulation**
1. Start the Flappy Bird NEAT simulation:
   ```bash
   python flappy_bird_neat.py
   ```
---

## **Demo**

Here’s an example of how the AI agents evolve over generations to improve their performance:

### **Generation 1**:
- Birds perform poorly, usually hitting the first pipe right away.
- The neural networks are still underdeveloped, and most birds fail quickly.

### **Generation 10**:
- Some birds begin to survive longer, showing gradual improvement in their ability to avoid pipes.
- The AI starts learning basic patterns like timing jumps.

### **Generation 50**:
- The best birds can now navigate through multiple pipes, surviving for a longer period.
- These birds demonstrate that the evolutionary process has significantly improved the neural networks.

Below is a demo video or gif showing how the birds evolve over time:
![Flappy Bird AI Gameplay](demo.gif)

In the video, you can observe the following:
- Early generations (1-10) display random, erratic movements.
- Later generations (50+) show more deliberate actions, with birds navigating pipes and avoiding obstacles more efficiently.

---

## **Future Work**

1. **Enhanced Inputs**:
   - Incorporate additional features into the neural network input, such as the bird's velocity or the proximity to the ground.
   - Experiment with providing more context to the network for improved decision-making.

2. **Save and Load Trained Models**:
   - Implement functionality to save the trained neural network models at the end of training.
   - This would allow users to resume training or deploy a pre-trained model for real-time gameplay.

3. **Advanced Fitness Functions**:
   - Experiment with custom fitness functions that not only reward survival time but also optimize for better navigation, fewer jumps, or less energy consumption.

4. **Multiplayer AI**:
   - Create a scenario where multiple AI birds can play the game at once, either cooperatively or competitively.
   - Introduce shared or competing fitness functions and observe interactions between multiple agents.

---

## **References**

- [NEAT-Python Documentation](https://neat-python.readthedocs.io/en/latest/)
- [Flappy Bird Clone by Tech with Tim](https://github.com/techwithtim/NEAT-Flappy-Bird)
- [NeuroEvolution of Augmenting Topologies (NEAT)](http://www.cs.ucf.edu/~kstanley/neat.html)

---

Feel free to contribute by submitting issues or pull requests! Let's make this project better together.
