# Diffusion-Limited-Aggregation
2D Simulation modeling clustering of particles undergoing Brownian motion. The problem statement can be found here: http://people.duke.edu/~ccc14/sta-663-2018/index.html but is reproduced below for consistency.

A simulation of diffusion-limited aggregation -- a process where brownian motion particles tend to aggregate together. Physically this process phenomenologically describes several phenomena in nature -- electro deposition during a chemical process, growth of corals, crystal growth etc.

Mathematically, In this simulation, we have n random walkers. Each walker starts from row 0 and a random column number, and in each step, the walker increases the row number by 1 and randomly increments or decrements its column number by 1. If the column number of the walker exceeds the maximum or becomes negative, the walker emerges on the other side (toroidal boundary conditions). At any time, if any of the walkers 8 neighbors is non-zero, the walker stops in that position, and the number of steps taken is recorded in that (row, column).

Write a function dla(nwalkers, width, height, seed) that returns a matrix with shape (width, height) after running nwalkers random walks as described above. The argument ssed is used to initialize a random number seed. Internally, the function should create a (width, height+1) matrix, and initialize the last row to have 1 with all other entries 0.
