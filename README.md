# colliding-random-walks
A repository for multiple particles colliding random walks, where 1s and 0s are the same. It simulates the diffusion of binary particles as a stochastic process.

[![DOI](https://zenodo.org/badge/661829288.svg)](https://zenodo.org/badge/latestdoi/661829288)

![Alt Text](https://github.com/calmendares1/colliding-random-walks/blob/main/MPRW%20110x110%20200%20sims.gif)

Animated is a 110x110 system with particles and antiparticles mixing over 200 time steps. The code generalizes random walks to any number of particles in any number of dimensions, but rendering an animation only works in 2D. Empty space is expressed through Boolean duality. Since particles and antiparticles are treated similarly, negating inputs negates outputs. A single particle in empty space (or a sea of antiparticles) is equivalent to a bounded random walk.

A system of size $N$ with $k$ particles and $n-k$ antiparticles has ${N} \choose {k}$ possible permutations. This gives an interesting interpretation of the state space because it has a total of ${{N} \choose {k}}^2 = \theta$ entries. Changes in the system can be represented as a Markov chain along the state space using a square stochastic matrix $P_{\theta \times \theta}$.

The Rmd files require certain R packages to render the MPRWs, but only the "reshape2" package is needed in order to run the simulation. I recommend exporting to csv files or *recoding in another programming language*. The benefit of R is rapid prototyping, the downside is that generalization is slow. See the attached preprint research paper "Multiple particles colliding random walks" for a more detailed analysis of colliding random walks.

The most unusual property of colliding random walk simulations is the nonuniform frequency of states. The stationary distribution of a colliding random walks simulation with a single particle (in an antiparticle box) is the uniform distribution. However, this is clearly not the case for colliding random walks.

![Alt Text](https://github.com/calmendares1/colliding-random-walks/blob/main/4x4%20Exit%20Counter%2C%20100%20sims%20per%20state.png)


The plot shows the number of incoming states out of 1000 simulations of a 4x4 system with 12870 possible states. Although 1000 simulations are not nearly enough to cover all states leading into a incoming state, it is clear that some states are preferred more than others. The *most incoming* state is the checkerboard and its inversion.

Below is a comparison of a 34x34 system with various animations


# Boolean Diffusion (34x34)
https://github.com/calmendares1/colliding-random-walks/assets/57421056/5a1d88a1-4537-4417-8ab5-21e78c5767e9

# Boolean Diffusion Smoothed
https://github.com/calmendares1/colliding-random-walks/assets/57421056/8acb02c5-5c83-4e70-abf7-d7d9facde4c9

# Boolean Diffusion, Boundary Emphasized
https://github.com/calmendares1/colliding-random-walks/assets/57421056/46541365-bb0c-4a60-94d5-1363d36038ec

# FFT of Boolean Diffusion
https://github.com/calmendares1/colliding-random-walks/assets/57421056/a233b300-79e4-4ea4-ba36-adde97a7f984



The Rmd files contain detailed comments for each and every single function and section as to hypothesis, code intention, and execution.

