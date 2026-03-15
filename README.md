# Financial Engineering: Derivatives Pricing & Numerical Analysis

## Project Overview
[cite_start]This repository contains the implementation and numerical analysis of pricing models for plain-vanilla and exotic derivatives[cite: 607, 609]. [cite_start]The project evaluates convergence rates, computational stabilities, and financial sensitivities (Greeks) of various numerical methods[cite: 607, 608, 609].

## Mathematical Models & Methodologies
* [cite_start]**Closed-Form Solutions**: Standard Black-Scholes framework for European options and the Bachelier (Normal) model for forward prices assuming negative values ($dF_t = \sigma_N dW_t$)[cite: 864, 866, 871].
* [cite_start]**Cox-Ross-Rubinstein (CRR) Binomial Trees**: Discrete-time pricing implementations for European, American, Barrier (Up-and-Out), and Bermudan options[cite: 607, 609, 684, 822].
* [cite_start]**Monte Carlo (MC) Simulations**: Risk-neutral path generation for European and path-dependent barrier options, enhanced with variance reduction techniques[cite: 607, 686, 792].

## Key Results & Financial Analysis
* [cite_start]**Error Scaling & Convergence**: Demonstrated empirically on a log-log scale that the numerical pricing error for European Calls scales as $1/M$ for the CRR tree and $1/\sqrt{M}$ for the MC approach[cite: 645, 646, 671, 672]. [cite_start]To meet a market bid/ask tolerance of $0.5 \cdot 10^{-4}$ (0.5 bp), the MC approach required $M=2^{20}$ simulations[cite: 634, 635, 639].
* [cite_start]**Barrier Options & Computational Instability**: Priced European Up&Out options and analyzed Vega sensitivity, noting a sign change as the underlying approaches the barrier[cite: 692, 695, 698]. [cite_start]Identified and explained the "sawtooth" effect—a severe computational instability in CRR Greek calculations caused by the discrete barrier payoff discontinuity expanding over the tree grid[cite: 730, 736, 737].
* [cite_start]**American vs. European Dynamics**: Showed that continuous barrier monitoring makes the American Up&Out Call strictly cheaper ($0.0147$ Euro) than its European counterpart ($0.0154$ Euro)[cite: 744, 746, 747, 752]. [cite_start]The Delta drops to exactly zero when the underlying hits the Knock-Out level ($S_0 \ge 1.4$)[cite: 780, 781].
* [cite_start]**Early Exercise Premium**: Compared Bermudan and European Calls, proving that when the risk-free rate ($2.5\%$) strictly exceeds the continuous dividend yield ($2\%$), the early exercise premium is near zero, making early exercise suboptimal[cite: 829, 830, 856].
* [cite_start]**Variance Reduction**: Successfully implemented the antithetic variables technique, exploiting the martingale property of the Wiener process to generate symmetric paths and reduce the standard error of the MC estimator[cite: 792, 793, 794, 795].

## Technologies & Libraries
* [cite_start]**Languages**: Python, MATLAB[cite: 610, 625].
* [cite_start]**Libraries**: NumPy, Pandas, Matplotlib, SciPy, and QuantLib (used for standard 30/360 year fractions and Modified Following schedules)[cite: 610, 960, 963].
