## Project Overview

This project models the genetic toggle switch, a foundational synthetic biology circuit first built by Gardner, Cantor, and Collins (2000), in which two genes are engineered to mutually repress each other. That single feedback loop is enough to create bistability: the system settles into one of two stable states and remains there, functioning as a form of cellular memory. The same wiring principle underlies natural cell-fate decisions, including stem cell differentiation.

Beyond reproducing the switch's core behavior, this project investigates why it works (through bifurcation analysis) and how robust it is to real biological noise (through stochastic simulation), connecting the deterministic model to the variability seen in real gene expression.

## Objectives

- Simulate the toggle switch's governing ODEs and confirm bistable behavior
- Visualize the system's phase portrait, nullclines, and basins of attraction
- Identify the cooperativity threshold required for bistability via bifurcation analysis
- Model gene expression noise and evaluate its effect on state-switching
- Build a reproducible, modular simulation codebase

## Methods and Tools

- Python
- NumPy
- SciPy (ODE integration, root finding)
- Matplotlib
- Euler-Maruyama stochastic integration

## Results

### Bistability and Phase Portrait

![Phase Portrait](https://fraede.github.io/Portfolio/assets/images/toggle-switch-project_phase_portrait.png)

The system converges to one of two stable steady states depending on initial conditions, visualized here with nullclines and the vector field.

### Bifurcation Analysis

![Bifurcation Diagram](https://fraede.github.io/Portfolio/assets/images/toggle-switch-project_bifurcation_diagram.png)

Sweeping the cooperativity parameter reveals a pitchfork bifurcation: below a critical threshold, only one steady state exists; above it, two new stable states emerge. This is the quantitative reason repressor proteins must bind DNA cooperatively for a switch to function.

### Noise-Induced Switching

![Stochastic Population](https://fraede.github.io/Portfolio/assets/images/toggle-switch-project_stochastic_population.png)

Sixty identical noisy trials from the same near-symmetric starting point split roughly evenly between the two stable states, demonstrating that gene expression noise alone can determine cell fate near the decision boundary.

## Key Skills Demonstrated

- Dynamical systems modeling and ODE simulation
- Bifurcation and stability analysis
- Stochastic differential equation methods
- Scientific computing with Python
- Translating systems biology concepts into computational models

## Repository

[View the GitHub Repository](https://github.com/Fraede/genetic-toggle-switch)

## Takeaways

This project deepened my understanding of how network topology alone, independent of any single component, can produce emergent behaviors like bistability. It also highlighted the importance of connecting deterministic models to biological reality: real cells are noisy, and understanding how that noise interacts with a circuit's dynamics is essential to predicting its behavior in vivo.
