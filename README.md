# Binary-Optimisation Model

This project presents an optimisation model designed to determine the most cost-efficient distribution of a pool of 45,000 tools across six storage sites.  
The objective is to minimise total operational costs while maintaining service-level targets for tool availability and response time.

The model determines optimal tool storage across multiple locations, considering factors such as capacity, distance, and service-level requirements.  
It formulates the problem as a binary integer programme, solved by a greedy heuristic which iterates over all tools in three phases.

All data used in the original industrial case are confidential and therefore not included in this repository.  
For the same reason, data preprocessing steps are also omitted.  
Only the heuristic model structure and logic are presented in the Heuristic Solution file. 
 


