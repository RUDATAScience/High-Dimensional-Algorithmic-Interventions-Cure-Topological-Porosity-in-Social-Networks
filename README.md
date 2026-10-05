# Simplicial Topological Mean Field Game (TMFG) for Network Resilience

This repository contains the computational simulation code for modeling consensus collapse and structural recovery in large-scale, scale-free social networks. By integrating **Algebraic Topology (Simplicial Complexes)** with **Stochastic Differential Equations (Mean Field Games)**, this project demonstrates that information pollution ruptures community consensus (2-simplices) rather than simply severing individual ties (1-simplices).

We mathematically prove that traditional 1-dimensional algorithmic interventions (e.g., edge recommendation systems) fundamentally fail to heal social fragmentation, and we establish the efficacy of high-dimensional interventions (2-simplex bypass surgeries) to cure topological porosity.

## Overview of the Framework

Current digital platforms combat social fragmentation using classical graph theory, recommending pairwise connections (edges) to bridge divided populations. This framework proves this paradigm is flawed. Using the Simplicial TMFG model (up to $N = 10,000,000$ nodes), we demonstrate:
1. **Consensus Collapse is a Topological Phenomenon:** Pathogenic information creates $\beta_1$ topological defects (holes) by rupturing shared 2-dimensional consensus spaces, not just 1-dimensional edges.
2. **1D Interventions Geometrically Fail:** Guided by the Euler-Poincaré formula, injecting edges without forming structured faces exacerbates macroscopic porosity.
3. **High-Dimensional Bypass is Required:** Strategic injection of 2-simplices (triadic closures) successfully shrinks the kernel of the Hodge Laplacian, achieving scale-invariant recovery.

## Repository Structure and Validations

The codebase is divided into several simulation scripts, each validating a specific hypothesis or structural constraint. All simulations are highly optimized using `Numba` (JIT compilation) and `SciPy` sparse matrices, allowing for massive macroscopic scale integration.

### 1. Core Hypotheses (Empirical Validations)
- **`Hypothesis1_Simplicial_TMFG.py` (Autonomic Stability & Hysteresis):** 
  Initializes the network using an uncalibrated continuous uniform distribution ($X_{i,0} \sim \mathcal{U}(0, 0.2)$). Proves autonomic self-organization using Kolmogorov-Smirnov (KS) tests and demonstrates irreversible topological hysteresis after pathogenic exposure.
- **`Hypothesis2_1D_Failure.py` (Failure of 1D Interventions):**
  Simulates classical edge recommendation systems. Proves that injecting 1-simplices equivalent to 10% of the network deterministically exacerbates the $\beta_1$ defect ratio by exactly $+0.200$.
- **`Hypothesis3_2D_Recovery.py` (High-Dimensional Bypass Surgery):**
  Simulates the targeted injection of 2-simplices. Demonstrates an instantaneous, scale-invariant reduction of approximately 95% of accumulated topological defects.

### 2. Advanced Validations (Robustness & Constraints)
- **`Adv_Validation_Dynamic_Network.py` (Time-Lagged Rupture):**
  Introduces adaptive rewiring dynamics. Proves that community consensus collapse ($\beta_1$ face rupture) strictly precedes individual unfollowing ($\beta_0$ edge severing), establishing a deterministic temporal window for intervention.
- **`Adv_Validation_Cult_SideEffect.py` (Cult Formation Penalty):**
  Evaluates the therapeutic trade-off. Demonstrates that forcing absolute eradication of social voids ($\beta_1 \to 0$) combinatorially synthesizes closed 3-simplices ($\beta_2$), mapping to isolated cultic echo-chambers.
- **`Adv_Validation_Heterogeneity.py` (Robustness to Nodal Variance):**
  Assigns nodal frustration thresholds from a statistical distribution ($\theta_i \sim \mathcal{N}(\mu_\theta, \sigma_\theta^2)$). Proves that the recovery mechanics of the Hodge Laplacian remain universally robust without requiring behavioral homogenization or empirical parameter tuning.

## Dependencies

The simulations require the following Python libraries:
- `numpy`
- `scipy`
- `matplotlib`
- `pandas`
- `numba`
- `tqdm`

To install the required packages:
```bash
pip install numpy scipy matplotlib pandas numba tqdm


OutputsUpon execution, each script generates:.csv files containing normalized topological defect tracking across all time steps..png visualizations mapping phase transitions (Burn-in, Pathogenesis, Hysteresis, and Intervention).A .zip archive aggregating all logs, summary statistics, and plots for macro-scale networks ($N=10^3$ to $N=10^7$).

License　This project is licensed under the MIT License - see the LICENSE file for details.
