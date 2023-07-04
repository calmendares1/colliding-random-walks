# colliding-random-walks
A repository for multiple particles colliding random walks, where 1s and 0s are the same. Stochastic binary diffusion equation.

[![DOI](https://zenodo.org/badge/661829288.svg)](https://zenodo.org/badge/latestdoi/661829288)

![Alt Text](https://github.com/calmendares1/colliding-random-walks/blob/main/MPRW%20100x100%20100%20sims%2010-90%20White%20to%20Brown%20noloop.gif)

The Rmd files require certain R packages to render the MPRWs, but only the "reshape2" package is needed in order to run the simulation. I recommend exporting to csv files or *recoding in another programming language*. The benefit of R is rapid prototyping, the downside is that generalization is slow. See the attached preprint research paper "Multiple particles colliding random walks" for a more detailed analysis of colliding random walks.

While the formal algorithm description is necessary, I would argue that the gif animations tell a better story.

![Alt Text](https://github.com/calmendares1/colliding-random-walks/blob/main/MPRW%20100x100%20100%20sims%2050-50%20White%20to%20Brown%20noloop.gif)

The Rmd files contain detailed comments for each and every single function and section as to hypothesis, code intention, and execution.

Apologies for the disorganization of the latest version of the file. It was originally constructed as a "do it all" kind of Rmd file. It suffers from a lot of bloat.
