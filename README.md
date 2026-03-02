# Binary Integer Optimisation — Capacity & SLA-Constrained Allocation

This project formulates a large-scale **binary integer allocation problem** for assigning tools to storage locations under cost, capacity, and service-level (SLA) constraints.

The objective is to minimise total expected cost (storage, handling, cleaning, maintenance) subject to:

- binary assignment: each tool assigned to exactly one location  
- location capacity constraints  
- SLA response-time constraints  

The natural formulation is a **Binary Integer Linear Program (BILP)**.  
As exact solving becomes computationally expensive at scale, a constraint-aware greedy heuristic is implemented to generate high-quality feasible solutions efficiently.

---

## Model Structure

Let:

- \( x_{i,j} \in \{0,1\} \): tool \(i\) assigned to location \(j\)

Objective:
\[
\min \sum_{i,j} c_{i,j} x_{i,j}
\]

Subject to:

- \( \sum_j x_{i,j} = 1 \quad \forall i \)
- \( \sum_i a_i x_{i,j} \leq \text{capacity}_j \quad \forall j \)
- SLA feasibility constraints per tool–location pair

---

## Heuristic Design

**Phase 1 — Cost Evaluation**  
Compute unconstrained and SLA-feasible costs for all tool–location pairs.

**Phase 2 — SLA-Constrained Allocation**  
Prioritise high-impact tools and allocate SLA-feasible assignments under capacity limits.

**Phase 3 — Capacity Completion**  
Assign remaining tools to lowest-cost feasible locations while respecting capacity.

The heuristic is designed to preserve feasibility while approximating the structure of the full BILP.

---

## Technical Highlights

- Binary integer optimisation formulation  
- Cost decomposition and trade-off modelling  
- Constraint-aware greedy algorithm design  
- Scalability considerations for large problem instances  

Industrial data are confidential and excluded; the repository contains the core optimisation logic only.

---

## How to run

1) Install dependencies:

```bash
pip install -r requirements.txt
```

2) Run the optimisation:

```bash
python src/heuristic_solution.py
```
