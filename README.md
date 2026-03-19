# RouteOpt: Optimal Route Selection using ADMM

RouteOpt is a numerical optimization project that addresses the shortest path problem using the Alternating Direction Method of Multipliers (ADMM). The project reformulates the classical graph-based routing problem into a constrained optimization framework and compares its performance with Dijkstra’s algorithm.

This work demonstrates how optimization techniques can be applied to scalable and distributed systems where traditional algorithms face limitations.

## Objectives
- Formulate the shortest path problem as a mathematical optimization problem
- Implement Dijkstra’s algorithm as a baseline
- Solve the problem using ADMM
- Analyze convergence and feasibility
- Compare performance between classical and optimization-based approaches

## Methodology
1. Graph Construction  
   A 10x10 grid graph is generated with weighted edges representing a network.

2. Baseline Algorithm  
   Dijkstra’s algorithm is used to compute the exact shortest path.

3. Optimization Formulation  
   The problem is expressed as:
   - Objective: Minimize total edge cost  
   - Constraints: Flow conservation across nodes

4. ADMM Implementation  
   The optimization problem is solved iteratively using:
   - Primal updates  
   - Auxiliary variable updates  
   - Dual variable updates  

5. Evaluation  
   Results are compared based on path cost, convergence behavior, and scalability.

## Results
| Method     | Path Cost | Path Length |
|------------|----------|------------|
| Dijkstra   | 34.72    | 18         |
| ADMM       | 34.75    | 18         |

ADMM converges close to the optimal solution while enabling distributed and parallel computation.

## Key Insights
- Dijkstra provides exact solutions but is limited to centralized systems
- ADMM offers scalability and is suitable for distributed environments
- Optimization-based approaches can effectively approximate graph solutions

## Tech Stack
- Python
- NumPy
- Graph Algorithms
- Numerical Optimization (ADMM)

## Project Report
The detailed project report is available below:

[View Full Report](./NOP_Report.pdf)
