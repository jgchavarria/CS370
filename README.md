# CS 370 Portfolio: Pirate Intelligent Agent

This repository contains my Project Two Jupyter Notebook, in which an intelligent agent (a pirate) learns to navigate a maze and reach the treasure using deep Q-learning, a form of reinforcement learning built on a neural network.

## Reflection

### What work did I do on this project?

I was given the project framework: the `TreasureMaze` class, which defines the maze, the pirate's moves, rewards, and game status; the `GameExperience` class, which stores episodes for experience replay; and starter notebook code for displaying the maze, building the neural network model, and checking whether the agent can win from every starting cell.

I wrote the core learning logic myself: the deep Q-learning training function (`qtrain`). Each epoch it starts the pirate in a random free cell, then chooses between a random valid move (exploration) and the model's best-predicted move (exploitation) using an epsilon-greedy policy. It records every move in the replay memory, samples a batch from that memory, and trains the network on it. I also added a rule that lowers epsilon to 0.05 once the win rate passes 90%, and I set the training parameters (1000 max epochs, a memory of 8 × the maze size, a batch size of 32, and a target network update every 50 epochs). Training stops only when the win rate reaches 100% **and** `completion_check()` confirms the pirate can reach the treasure from every starting cell. In my final run this happened at epoch 571, in about 13 minutes.

### What do computer scientists do and why does it matter?

Computer scientists solve real problems by designing, building, and testing computational systems. In this project, the problem was teaching an agent to make good decisions without hard-coding a path. That kind of work matters because the same ideas power robotics, logistics, game AI, and security tools that must adapt to changing conditions. Computing now touches nearly every industry, so the quality of what computer scientists build affects many people.

### How do I approach a problem as a computer scientist?

I start by defining the problem clearly: what the states, actions, and goals are. Then I break it into smaller pieces, pick a technique that fits (here, Q-learning with a neural network), build a working version, and test it. When results fall short, I change one variable at a time and measure the effect, as I did when adjusting exploration and training settings. I also build on existing tools and libraries instead of starting from scratch, and I document my work so others (and my future self) can follow it.

### What are my ethical responsibilities to the end user and the organization?

To the end user, I owe software that is safe, honest, and respectful of their privacy, and I should be open about what a system can and cannot do. Learning systems especially can behave in unexpected ways, so thorough testing matters before anyone relies on them. To the organization, I owe quality work, honesty about limitations and risks, protection of its data, and respect for licenses and intellectual property. Where those two duties conflict, I should raise concerns instead of hiding problems. As someone interested in cybersecurity, I take these responsibilities seriously because mistakes in the systems I build can harm real people.
