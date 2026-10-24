# CS 370 Portfolio: Pirate Intelligent Agent

This repository contains my Project Two Jupyter Notebook, in which an intelligent agent (a pirate) learns to navigate a maze and reach the treasure using deep Q-learning, a form of reinforcement learning built on a neural network.

## Reflection

### What work did I do on this project?

I was given the project framework: the `TreasureMaze` class, which defines the maze, the pirate's moves, rewards, and game status; the `GameExperience` class, which stores episodes for experience replay; and starter notebook code for displaying the maze, building the neural network model, and checking whether the agent can win from every starting cell.

I wrote the core learning logic myself: the deep Q-learning training function (`qtrain`). It runs training episodes, chooses between exploration and exploitation with an epsilon-greedy policy, records each experience, samples batches from memory, trains the network on updated Q-value targets, and stops once the agent wins consistently from every starting position. I also tuned the training parameters (epsilon, epochs, memory size, and batch size) and tested the results so the pirate reliably found the treasure.

### What do computer scientists do and why does it matter?

Computer scientists solve real problems by designing, building, and testing computational systems. In this project, the problem was teaching an agent to make good decisions without hard-coding a path. That kind of work matters because the same ideas power robotics, logistics, game AI, and security tools that must adapt to changing conditions. Computing now touches nearly every industry, so the quality of what computer scientists build affects many people.

### How do I approach a problem as a computer scientist?

I start by defining the problem clearly: what the states, actions, and goals are. Then I break it into smaller pieces, pick a technique that fits (here, Q-learning with a neural network), build a working version, and test it. When results fall short, I change one variable at a time and measure the effect, as I did when adjusting exploration and training settings. I also build on existing tools and libraries instead of starting from scratch, and I document my work so others (and my future self) can follow it.

### What are my ethical responsibilities to the end user and the organization?

To the end user, I owe software that is safe, honest, and respectful of their privacy, and I should be open about what a system can and cannot do. Learning systems especially can behave in unexpected ways, so thorough testing matters before anyone relies on them. To the organization, I owe quality work, honesty about limitations and risks, protection of its data, and respect for licenses and intellectual property. Where those two duties conflict, I should raise concerns instead of hiding problems. As someone interested in cybersecurity, I take these responsibilities seriously because mistakes in the systems I build can harm real people.
