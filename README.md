# silas.a.ayariga-pythonreport
# Mathematical Modeling of Smoking Dynamics

This project implements a compartmental model to simulate the dynamics of smoking within a population. Using systems of Ordinary Differential Equations (ODEs), the model explores how the "smoking habit" spreads or declines based on transmission rates and quitting rates.

## Overview

The model categorizes the population into two proportions:
- **x**: Potential Smokers
- **y**: Current Smokers

The system is governed by the following equations:
- $dx/dt = \mu (1 - x) - \beta x y$
- $dy/dt = y (\beta x - \mu - \gamma)$

Where:
- $\mu$: Population exit/death rate.
- $\beta$: Contact/Transmission rate.
- $\gamma$: Quitting rate.

### Key Concepts
- **Basic Reproduction Number ($R_0$):** Calculated as $\beta / (\mu + \gamma)$.
- **Smoke-Free Equilibrium:** When $R_0 < 1$, the smoking population eventually disappears.
- **Endemic Equilibrium:** When $R_0 > 1$, the smoking habit persists at a stable level.

## Visualization
The simulation generates phase portraits showing trajectories from various initial conditions toward stable equilibria.

## Installation
```bash
pip install numpy matplotlib scipy

python smoking_model.py
