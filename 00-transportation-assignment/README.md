# Transportation & Assignment Problems

🚧 Project in progress

## Business Problem
A company operates multiple warehouses and serves several customer regions.
Each warehouse has limited supply capacity, and each region has a known demand.
Transportation costs vary between warehouse–region pairs.

## Goal
Determine the optimal shipment quantities from each warehouse to each region
that minimize total transportation cost.

## Constraints
- Each warehouse cannot ship more than its available supply.
- Demand at each customer region must be fully satisfied.
- Shipment quantities must be non-negative.

## Implementation Plan
- LP formulation using Pyomo
- Solver comparison: CBC vs CPLEX (Community Edition)
- Sensitivity and cost analysis

**Status:** Model formulation and solver setup in progress
