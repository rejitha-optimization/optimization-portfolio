# Transportation Problem

## Problem Overview
This project demonstrates the transportation optimization problem, a
fundamental Operations Research model widely used for cost-efficient logistics
and resource allocation.

The objective is to determine optimal shipment quantities from multiple
warehouses to multiple customer regions such that total transportation cost is
minimized, while satisfying supply and demand constraints.

## Mathematical Formulation
The transportation problem is formulated as a linear program with:
- Continuous decision variables representing shipment quantities
- A linear cost minimization objective
- Supply capacity constraints at warehouses
- Demand satisfaction constraints at customer regions

## Implementation
- Modeling framework: Pyomo (Python)
- Solvers:
  - CBC (open-source baseline)
  - CPLEX (Community Edition)

The same mathematical formulation is reused for the small illustrative
example and the large-scale transportation scenario.

## Results
Both CBC and CPLEX return identical optimal objective values, confirming model
correctness and solver portability across different LP solvers.

## Insights
- Transportation problems can be efficiently modeled as linear programs to
  support cost-efficient logistics decisions.
- A single formulation scales from small examples to larger, realistic problem
  instances.
- Solver-agnostic modeling enables flexibility in real-world optimization
  frameworks.

## Extensions
- Multi-period transportation
- Capacity expansion decisions
- Cost uncertainty and stochastic extensions


