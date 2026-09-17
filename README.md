# Bayesian Classification on Parametric Distributions

Random number generation, distribution testing, and Bayesian decision-theoretic classification, from one dimension up to three-dimensional multivariate Gaussians.

- [Notebook](Bayesian_Classification_on_parametric_distributions.ipynb)
- [Paper](Bayesian_Classification_on_parametric_distributions.pdf)

## Approach

**Part 1: Random number generation and distribution testing**
- Built a Linear Congruential Generator (LCG) from scratch to produce reproducible uniform random streams
- Generated normal, exponential, and Poisson variates from the uniform streams using inverse-transform sampling, the Box-Muller transform, and an error-function-based method
- Validated each generated distribution with the Pearson chi-square goodness-of-fit test and the runs test for randomness

**Part 2: Bayesian classification in one dimension**
- Derived and computed the theoretical decision boundary and probability of error for two-class problems using Bayes' decision rule with unequal priors, for uniform, normal, and mixed (Gaussian + uniform) class-conditional densities
- Simulated each scenario by drawing 20,000 samples per class and comparing the empirical probability of error against the theoretical value

**Part 3: Bayesian classification in multiple dimensions**
- Generated correlated multivariate Gaussian samples via Cholesky decomposition of specified covariance matrices
- Extended the classifier to two- and three-class problems in 2D and 3D under varying covariance structures (shared vs. distinct covariance per class)
- Computed theoretical classification boundaries and probability of error, then verified them by simulating classifier performance on the generated samples
