# Facility Location Optimization (Pyomo)

## Overview

This project implements the **Facility Location Problem (FLP)** using Pyomo.

The objective is to determine:

* Which facilities to open
* How to assign customers to facilities

such that the **total cost (opening cost + transportation cost)** is minimized.

---

## Problem Summary

* Strategic decision: facility selection
* Operational decision: customer assignment
* Trade-off:

  * More facilities → lower transport cost, higher opening cost
  * Fewer facilities → higher transport cost, lower opening cost

---

## Model

Formulated as a **Mixed-Integer Linear Program (MILP)**:

* Binary variables → facility opening
* Continuous variables → shipment decisions

Constraints:

* Demand satisfaction
* Capacity limits
* Facility must be open to serve

---

## Key Insight: LP vs MILP

* LP relaxation gives a **lower bound**
* Produces **fractional (non-realistic) solutions**
* MILP provides **implementable decisions**

---

## Features

* Synthetic data generation (spatial + demand-based)
* Visualization of facility-customer network
* LP vs MILP comparison
* Scalable pipeline for any problem size

---

## Scalable Pipeline

Run for any size:

```python
run_pipeline(n_facilities, n_customers)
```

---

## Key Takeaways

* Facility location combines **strategic + operational optimization**
* Captures real-world cost trade-offs
* Demonstrates MILP modeling and analysis
* Easily extendable to large-scale and real-world applications

---

## Note

This project is part of a structured effort to build a **portfolio of real-world optimization models** for industry applications.

