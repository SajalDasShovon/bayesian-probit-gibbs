# Bayesian Probit Regression using Gibbs Sampling

## Overview
This project implements a Bayesian probit regression model using latent variable augmentation and Gibbs sampling.

The model introduces a latent continuous variable Z such that:
Y = 1 if Z > 0, otherwise Y = 0.

## Model
Z_i = x_i'β + ε_i,   ε_i ~ N(0, σ²)

## Methods
- Bayesian inference with non-informative prior: p(β, σ²) ∝ 1/σ²
- Gibbs sampling:
  1. Sample Z (truncated normal)
  2. Sample β (normal posterior)
  3. Sample σ² (inverse-gamma posterior)

## Features
- Data simulation
- Gibbs sampler implementation in R
- Posterior estimation of parameters
- Computation of P(β₁ > 0 | Y)

## Results
The model estimates posterior distributions for β and σ² and evaluates the probability that β₁ > 0.

