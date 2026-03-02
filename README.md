# Binary Integer Optimisation — Capacity & Service-Level-Agreement Constrained Allocation

This project implements a large-scale **binary integer allocation model** for assigning tools to storage locations under cost, capacity, and service-level (SLA) constraints.

The objective is to minimise total cost (storage, handling, cleaning, maintenance) subject to:
- binary assignment (each tool assigned to exactly one location)
- location capacity constraints
- SLA response-time constraints

Because exact BILP solving becomes computationally expensive at scale, a constraint-aware greedy heuristic is implemented.

## Heuristic Structure

**Phase 1:** Evaluate all tool–location pairs and compute unconstrained and SLA-feasible costs.  
**Phase 2:** Prioritise high-impact tools and allocate SLA-feasible assignments under capacity limits.  
**Phase 3:** Assign remaining tools to cheapest feasible locations while respecting capacity.

## Technical Focus

- Binary integer optimisation logic  
- Cost decomposition and trade-off modelling  
- Constraint filtering and prioritised allocation  
- Scalable heuristic design for large problem instances  

Industrial data are confidential and excluded, the Heuristic Solution file contains the core optimisation logic only.
