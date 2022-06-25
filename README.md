# Tree-Disease-Spread-Cellular-Automata

We propose a system that models the spread of disease throughout the branches of individual fruit trees, in which we will compute the “optimal” shape that a tree should be pruned to prior to the onset of the disease. Our system is unique because of its scope- while several cellular automata (CA) models simulate the spread of disease among individual entities, we plan to model the spread of disease among different parts of a single entity. It will contain four major parts: (1) individual tree generation (in a grid space), (2) a CA to model disease spread, (3) model visualization, and (4) optimal tree shape computation. Our model can then open up the  possibility to explore several experiments, such as simulating the effects of fertilization or pollination on the spread of infection throughout a fruit tree. We hope to produce a novel computational approach to making tree maintenance decisions and provide insight into preventing disease spread in trees. 

## Conceptual Model
The basic conceptual model involves modeling the disease spread using a cellular automata system. This system should be modular and easy to update in terms of rules and parameters. We plan to create a bunch of trees during run simulation, run the CA model on the trees, and find the optimal shape of the tree based on best performance (least infection) during simulation. 

The first step would be to discretize the parts of a tree such as branches and leaves. We will represent the tree by a NxN grid, in which some cells will combine to form a branch while some will be empty. The tree corresponds to the cells that are not empty. 

We then study the spread of a generic disease which originates at the leaves and spreads to other leaves through the branches. An infection can start at more than one spot in the tree and spread out from there. The rate of spread of disease is different within the leaves (faster) and in the branches (slower).  Each part of the tree is in one of the following states: 
Healthy
Infected
Dead

A tree is said to be dead when more than 75% of its parts are in “dead” state.

The rate at which the disease spreads is altered by the natural immune response of the tree and the use of fungicides / insecticides on the leaves. The immune response is a function of the tree’s ‘health’, and goes down as more parts of the tree become infected or dead.


