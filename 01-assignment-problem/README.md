# Assignment Problem: Cost-Optimal Worker-Task Allocation 

## Problem Overview
The assignment problem is a classical optimization model in Operations Research that focuses on matching a set of workers to a set of tasks in a cost-optimal manner. Each possible worker-task assignment incurs a known cost, and the objective is to determine a one-to-one matching that minimizes the total assignment cost.

---

## Business Motivation
Assignment-type decisions arise frequently in real-world operational settings, such as:
- Assigning employees to jobs
- Assigning machines to tasks
- Assigning drivers to delivery routes
- Assigning reviewers to evaluation tasks.

In these scenarios, decision-makers must allocate limited resources efficiently while ensuring that each task is handled by exactly one resource.

---

## Modeling Approach
The problem is formulated as MILP (Mixed Integer Linear Program) with binary decision variables indicating whether a resource is assigned to a specific task.
The model enforces:
- Exactly one worker assigned to each task
- At most one task assigned to each worker.

The formulation is implemented using Pyomo in Python and solved using mixed-integer linear programming solvers:

- **CBC** as an open-source baseline solver
- **CPLEX (Community Edition)** to demonstrate solver portability.

Both solvers return identical optimal objective values for the illustrative example, confirming the correctness and solver-independence of the formulation.

---

## LP Relaxation Analysis
To highlight the role of integrality, the LP relaxation of the assignment model is also examined by allowing decision variables to take continuous values between 0 and 1. While the relaxed model may achieve comparable objective values, the resulting fractional assignments lack a clear operational interpretation.

This analysis demonstrates why binary constraints are essential for enforcing meaningful, discrete assignment decisions in practice.

---

## Scalability Demonstration
The same assignment formulation is applied to a large-scale assignment scenario using a programically generated cost matrix. The model and implementation remain unchanged, with scalability achieved solely through expanded input data.

This demonstrates the generality and reusability of the formulation and the modular design of the Pyomo implementation.

---

## Key Takeaways
- The assignment problem can be effectively modeled as a MILP to support cost-efficient resource allocation.
- The formulation is solver-agnostic, yielding consistent solutions across open-source and commercial solvers.
- Integrality constraints play a critical role in producing meaningful assignment decisions.
- The model scales naturally to large scale problem instances without modification to the underlying formulation or implementation.

This project serves as a foundational building block for more advanced scheduling, allocation, and matching problems.

