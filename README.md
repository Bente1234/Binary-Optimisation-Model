# Binary-Optimisation-Model
This is a thesis project which presents an optimisation model for determining the most cost-efficient distribution of a pool of 45,000 tools across six storage sites.  
The objective is to minimise total operational costs while maintaining service-level targets for tool availability and response time.

All data used in the original case are confidential and therefore not included in this project. Only the model logic and code structure are provided.

The project models how tools should be stored across several potential locations, considering factors such as capacity, distance, and service-level requirements.  It formulates the problem as a binary integer programme solved by a Greedy Heuristic which iterates over all tools in three phases. 

