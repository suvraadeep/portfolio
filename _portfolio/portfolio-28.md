---
title: "Dynamic What-if Scheduling"
excerpt: "A machine learning-powered scheduling and scenario analysis system for construction projects. It predicts activity completion, simulates delays, and enables interactive what-if planning using DAGs, Monte Carlo simulation, and ensemble models."
collection: portfolio
---

🔗 **GitHub Repo:** [Dynamic What-if Scheduling](https://github.com/suvraadeep/Dynamic-What-if-scheduling)  


### Key Features:
1. **Ensemble Schedule Prediction**: Combines earned-value extrapolation + Gradient Boosting + Monte Carlo simulation for accurate completion forecasts.
2. **What-if Scenario Engine**: Simulates delays, resource boosts, issue resolution, and parallel execution to evaluate schedule impact.
3. **Delay Propagation (Ripple Engine)**: Uses DAG-based BFS traversal to propagate delays across dependent activities.
4. **Critical Path Optimization**: Implements CPM to identify zero-float activities and generate rule-based optimization strategies.
5. **Interactive Dashboard**: Streamlit-based UI with Gantt charts, DAG visualization, and scenario comparison tools.  


### Example Workflow:
#### Scenario: *"What if plumbing is delayed by 7 days?"*
1. **Dependency Graph**: Builds DAG of activity dependencies.
2. **Ripple Simulation**:
   - Propagates delay across downstream tasks.
3. **Output**:
   - Updated project end date + affected activities.

#### Scenario: *"Can we recover delay by adding resources?"*
1. **Resource Boost Simulation**:
   - Reduces activity duration.
2. **Recompute Schedule**:
   - Applies CPM + ripple adjustments.
3. **Output**:
   - Time saved + estimated cost impact.


### Screenshots:

#### Overview
![Overview](https://github.com/suvraadeep/Dynamic-What-if-scheduling/blob/main/screenshots/overview.png)

#### Gantt Chart
![Gantt](https://github.com/suvraadeep/Dynamic-What-if-scheduling/blob/main/screenshots/gantt.png)

#### Predictions
![Predictions](https://github.com/suvraadeep/Dynamic-What-if-scheduling/blob/main/screenshots/predictions.png)

#### Ripple Analysis
![Ripple](https://github.com/suvraadeep/Dynamic-What-if-scheduling/blob/main/screenshots/ripple.png)

#### What-if Scenarios
![What-if](https://github.com/suvraadeep/Dynamic-What-if-scheduling/blob/main/screenshots/whatif.png)

#### DAG Visualization
![DAG](https://github.com/suvraadeep/Dynamic-What-if-scheduling/blob/main/screenshots/dag.png)

#### Optimization & Critical Path
![Optimization](https://github.com/suvraadeep/Dynamic-What-if-scheduling/blob/main/screenshots/optimization.png)


### Technologies Used:
- **Python (Pandas, NumPy)**: Data processing and pipeline.
- **Scikit-learn**: Gradient Boosting model for delay prediction.
- **NetworkX**: DAG construction and traversal.
- **SciPy**: Monte Carlo simulation.
- **Plotly & Matplotlib**: Visualization (Gantt, DAG).
- **Streamlit**: Interactive web dashboard.
- **SQLite & SQLAlchemy**: Data storage and management.
