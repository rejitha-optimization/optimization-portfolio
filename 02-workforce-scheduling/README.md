# Workforce Scheduling with Optimization

## Overview
This project presents an industry-inspired workforce scheduling problem
formulated and solved using mathematical optimization. The goal is to
assign workers to shifts while satisfying operational requirements such
as staffing requirement, skill coverage, availability constraints, and
assignment limits.

The project demonstrates how optimization models can be used not only to
generate feasible schedules, but also to improve schedule quality through
the inclusion of soft constraints such as worker preferences and fairness
considerations.

---

## Business Problem
Organizations operating with shift-based labor must ensure that each
shift is adequately staffed with qualified personnel while respecting
worker availability and operational policies. In practice, multiple
feasible schedules may exist, and decision-makers often wish to favor
assignments that better align with worker preferences or fairness goals.

This project addresses the following questions:
- How can workforce scheduling requirements be modeled as an optimization
  problem?
- How can feasibility constraints be enforced rigorously?
- How can qualitative considerations be incorporated without sacrificing
  feasibility?

---

## Mathematical Formulation
The workforce scheduling problem is formulated as a binary mixed-integer
linear program (MILP).

- **Decision variables** represent whether a worker is assigned to a
  particular shift.
- **Hard constraints** enforce staffing requirements, skill coverage,
  worker availability, and assignment limits.
- **Soft constraints** are introduced as penalty terms in the objective
  function to capture worker preferences and fairness considerations.

This separation between feasibility and quality reflects common practice
in real-world scheduling applications.

---

## Implementation Details
- **Modeling framework:** Pyomo (Python)
- **Problem type:** Binary MILP
- **Solvers used:**
  - CBC (open-source)
  - CPLEX (Community Edition)

The implementation follows a modular design:
- Data is defined separately from the model
- The core feasibility model is constructed first
- Soft constraints are added by modifying the objective function
- The same formulation is solved using different solvers without changes

---

## Results and Insights
- The baseline model produces a feasible schedule that satisfies all
  operational constraints using the minimum number of assignments.
- Incorporating soft constraints improves schedule quality by favoring
  preferred worker-shift assignments while maintaining feasibility.
- Both CBC and CPLEX return identical optimal objective values, confirming
  solver independence of the formulation.
- The model structure scales naturally to larger problem instances without
  modification to the underlying formulation.

---

## Key Modeling Insight
The scheduling model separates feasibility and quality by enforcing hard
constraints as strict requirements and modeling soft constraints through
penalties in the objective function. This approach allows flexible
trade-offs without compromising operational validity.


