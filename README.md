for Sir Michael's CSP323A/L activity, the instructions are at [INSTRUCTIONS.md](INSTRUCTIONS.md).

for the Google Doc contents, see [SESSION.md](SESSION.md).

# CSP323 Group 4 Aviation Optimization Demo

This repository contains the Group 4 notebook implementation for Philippine aviation route optimization using a Memetic Genetic Algorithm (GA + 2-opt local search), with Hill Climbing (HC) as a baseline.

## What This Codebase Does

- Solves a Traveling Salesman Problem (TSP)-style route planning task using real waypoint coordinates.
- Uses the Haversine formula for great-circle distance between waypoints.
- Compares HC versus Memetic GA performance.
- Produces visual analysis artifacts (maps, convergence plots, sensitivity analysis, and a summary dashboard).

## Repository Structure

- [INSTRUCTIONS.md](INSTRUCTIONS.md): Activity requirements and implementation checklist for the CSP323A/L task.
- [group4_advanced_GA_TSP_v2.ipynb](group4_advanced_GA_TSP_v2.ipynb): Main and latest notebook (primary implementation).
- [global_aviation_waypoints.csv](global_aviation_waypoints.csv): Source dataset of global aviation waypoints.
- [fig1_dataset_map.png](fig1_dataset_map.png) to [fig9_dashboard.png](fig9_dashboard.png): Generated figures from the main notebook.
- old images/: Archive folder containing previous notebook versions and older figure snapshots.

### Archive Folder Notes (old images)

- [old images/group4_advanced_GA_TSP.ipynb](old%20images/group4_advanced_GA_TSP.ipynb): Earlier advanced GA notebook version.
- [old images/group4-maindemo.ipynb](old%20images/group4-maindemo.ipynb): Main demo notebook from a prior stage.
- [old images/advanced_aviation_optimization.ipynb](old%20images/advanced_aviation_optimization.ipynb): Earlier expanded optimization case study.
- [old images/tsp_complete_advanced.ipynb](old%20images/tsp_complete_advanced.ipynb): Prior complete advanced TSP write-up notebook.

## Main Notebook Workflow

The notebook [group4_advanced_GA_TSP_v2.ipynb](group4_advanced_GA_TSP_v2.ipynb) is organized as a step-by-step pipeline:

1. Import libraries, load and clean the waypoint dataset, and sample Philippine waypoints.
2. Build map plotting helpers (Cartopy if available, fallback plotting if not).
3. Generate exploratory visuals for dataset geography and statistics.
4. Build a pairwise distance matrix using Haversine distance.
5. Define optimization operators:
	- route distance and fitness
	- population initialization
	- tournament selection
	- ordered crossover (OX)
	- swap mutation
	- 2-opt local search (memetic step)
6. Run Hill Climbing baseline with random restarts.
7. Run Memetic GA evolution loop.
8. Compare HC versus Memetic GA routes and convergence behavior.
9. Run parameter sensitivity checks and generate the final summary dashboard.

## Generated Outputs

Running the main notebook produces these figure files in the project root:

- [fig1_dataset_map.png](fig1_dataset_map.png): Global map plus Philippine zoom.
- [fig2_dataset_stats.png](fig2_dataset_stats.png): Dataset distribution/statistics panels.
- [fig3_distance_matrix.png](fig3_distance_matrix.png): Pairwise distance matrix and nearest-neighbor chart.
- [fig4_hc_baseline.png](fig4_hc_baseline.png): Hill Climbing baseline behavior.
- [fig5_convergence.png](fig5_convergence.png): Memetic GA convergence and diversity plots.
- [fig6_route_evolution.png](fig6_route_evolution.png): Route snapshots across generations.
- [fig7_route_comparison.png](fig7_route_comparison.png): HC versus Memetic GA final route comparison.
- [fig8_sensitivity.png](fig8_sensitivity.png): Parameter sensitivity analysis.
- [fig9_dashboard.png](fig9_dashboard.png): Final integrated dashboard.

## Dependencies

Core Python libraries used in the notebook:

- pandas
- numpy
- matplotlib
- scipy
- jupyter

Optional (for real coastline map rendering):

- cartopy

If Cartopy is unavailable, the notebook still runs with a built-in map fallback.

## How To Run

1. Keep [group4_advanced_GA_TSP_v2.ipynb](group4_advanced_GA_TSP_v2.ipynb) and [global_aviation_waypoints.csv](global_aviation_waypoints.csv) in the same folder.
2. Install dependencies in your Python environment.
3. Open the notebook and run cells from top to bottom.
4. Check generated figure files in the root directory after execution.

## Scope

This repository is notebook-centric and intended for CSP323 reporting/demonstration work rather than as a packaged Python module.
