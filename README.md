# Derivatives Pricing Models

## 📌 Project Overview
This repository contains a suite of Python and MATLAB scripts for pricing financial derivatives. The project focuses on implementing mathematical models to evaluate options, analyze numerical errors, and calculate Greeks.

## Mathematical Models Implemented
* **Analytical Pricing**: Closed-form solutions using functions like `blkprice` for European options.
* **Cox-Ross-Rubinstein (CRR) Binomial Trees**: Discrete-time models for pricing standard European options, barrier options, and Bermudan options.
* **Monte Carlo Simulations**: Stochastic simulations for pricing European options and path-dependent European barrier options (up-and-out).

## Key Features
* **Numerical Convergence Analysis**: Analysis demonstrating that numerical errors scale as 1/M for the CRR tree approach and as 1/\sqrt(M) for the Monte Carlo approach.
* **Greeks Calculation**: Computation and visualization of Greeks such as Delta and Vega over varying underlying prices.
* **Path-Dependent & Early Exercise features**: Handling of barrier options and Bermudan options, including the analysis of dividend yield impacts on early exercise.

## About
This project was developed as part of the Quantitative Finance / Financial Engineering curriculum at Politecnico di Milano.
