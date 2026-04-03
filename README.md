
# RouteOpt: Optimization and Learning-Based Route Selection

RouteOpt is a hybrid routing framework that addresses the shortest path problem using **classical algorithms, numerical optimization, and learning-based methods**. The project reformulates routing as a constrained optimization problem using ADMM and extends it with Graph Neural Networks (GNNs) and Generative AI for prediction and interpretability.

This work demonstrates how optimization and learning approaches can complement traditional graph algorithms in scalable and real-world routing scenarios.

---

## Objectives

* Formulate the shortest path problem as a constrained optimization problem
* Implement **Dijkstra’s algorithm** as the baseline
* Solve routing using **ADMM optimization**
* Apply **Graph Neural Networks (GNNs)** for learned route prediction
* Integrate **Generative AI** for explainable routing decisions
* Evaluate and compare all approaches using quantitative metrics

---

## Methodology

1. **Graph Construction**
   A weighted grid graph (10×10) is generated to simulate a routing network.

2. **Baseline Algorithm**
   Dijkstra’s algorithm computes the exact shortest path.

3. **Optimization Formulation**
   The routing problem is expressed as:

   * Objective: Minimize total edge cost
   * Constraints: Flow conservation across nodes

4. **ADMM Implementation**
   The optimization problem is solved iteratively using:

   * Primal updates
   * Projection (constraint enforcement)
   * Dual updates

5. **Learning-Based Routing (GNN)**
   A Graph Neural Network is trained to learn node importance and predict efficient routes.

6. **Explainability (Generative AI)**
   A language model generates structured explanations of routing decisions.

7. **Evaluation**
   Models are compared using cost, optimality gap, and convergence metrics.

---

## Results

### Path Comparison

| Method   | Path Cost | Path Length |
| -------- | --------- | ----------- |
| Dijkstra | 34.72     | 18          |
| ADMM     | 34.75     | 18          |
| GNN      | ~35–37    | Approx.     |

---

### Evaluation Metrics

| Metric               | Dijkstra (Baseline) | ADMM            | GNN              |
| -------------------- | ------------------- | --------------- | ---------------- |
| Path Cost            | Optimal             | Near-optimal    | Approximate      |
| Optimality Gap       | 0                   | Very Low        | Moderate         |
| Relative Error (%)   | 0                   | Low             | Moderate         |
| Feasibility Residual | N/A                 | → 0 (converges) | N/A              |
| Convergence Behavior | Immediate           | Iterative       | Not applicable   |
| Scalability          | Limited             | High            | Very High        |
| Interpretability     | Low                 | Medium          | High (via GenAI) |

---

## Key Insights

* **Dijkstra** guarantees exact optimality but lacks flexibility for constraints.
* **ADMM** provides a scalable optimization framework with strong convergence and near-optimal solutions.
* **GNN** enables fast, learning-based routing suitable for large or dynamic graphs.
* **Generative AI** improves transparency by explaining model decisions in natural language.

---

## Tech Stack

* Python
* NumPy
* PyTorch Geometric (GNN)
* Graph Algorithms
* ADMM Optimization
* Generative AI (Gemini API)

---

## Project Report

The detailed project report is available below:

[View Full Report](./NOP_Report.pdf)

