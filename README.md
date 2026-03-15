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
* 
## 📊 Key Results & Financial Analysis

* [cite_start]**Pricing & Error Convergence**: A standard European Call was successfully priced at 0.0163 Euro using the Black-Scholes analytical formula, CRR binomial trees, and Monte Carlo (MC) simulations[cite: 625, 626, 627]. [cite_start]Convergence analysis on a log-log scale confirmed that numerical errors rescale as $1/M$ for the CRR tree and $1/\sqrt{M}$ for the MC method. [cite_start]To meet a tolerance of 0.5 bp, the MC approach required $M=2^{20}$ simulations[cite: 634, 639].


* [cite_start]**Barrier Options & Computational Instability**: Priced a European Up&Out Call (Barrier at 1.4 Euro) at 0.0154 Euro[cite: 677, 680, 682]. [cite_start]The analysis of Vega revealed a sign change: it is positive when $S_0$ is between 0.65 and ~1.10, but becomes strongly negative as the underlying approaches the barrier[cite: 696, 698]. [cite_start]We also identified and explained the "sawtooth" effect—a severe computational instability in CRR Greek calculations caused by the discrete barrier payoff discontinuity[cite: 736].


* [cite_start]**American vs. European Barrier Dynamics**: Demonstrated that continuous monitoring makes the American Up&Out Call strictly cheaper (0.0147 Euro) than its European counterpart (0.0154 Euro)[cite: 746, 747, 752]. [cite_start]We plotted the Delta, showing it sharply drops to exactly zero when the underlying hits the Knock-Out level ($S_0 \ge 1.4$)[cite: 780, 781].

* [cite_start]**Bermudan Options & Dividend Impact**: The Bermudan Call price perfectly matched the European Call (0.0163 Euro)[cite: 824, 825]. [cite_start]We proved that because the risk-free rate (2.5%) was strictly greater than the dividend yield (2%), the early exercise premium is near to zero, making early exercise suboptimal[cite: 830, 856].

* [cite_start]**Variance Reduction & Financial Calendars**: Successfully implemented the antithetic variables technique to reduce the standard error of the MC estimator[cite: 792]. [cite_start]Additionally, utilized the QuantLib library to handle standard 30/360 year fractions and generate Modified Following business day schedules[cite: 960, 963].

## About
This project was developed as part of the Quantitative Finance / Financial Engineering curriculum at Politecnico di Milano.
