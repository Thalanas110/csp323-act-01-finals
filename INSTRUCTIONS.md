# Memetic Genetic Algorithm Task  (& Hill Climbing)
### Aircraft Route Optimization (TSP)

---

## Overview

An aircraft must travel from **Basa Air Base (RPUB)** and return to the same location while performing aerial inspections across multiple waypoints.

The objective is to determine the **shortest possible route** that visits all selected waypoints, considering constraints such as wartime fuel efficiency.

---

## Objectives

- Visit all inspection waypoints  
- Minimize total travel distance  
- Start and end at **RPUB (Basa Air Base, Pampanga)**  
- Maintain route validity (no missing or duplicated waypoints unless handled properly)  

---

## Given Data

- **Total PH Waypoints:** 373 (within Manila FIR)  
- **Selected Waypoints (TSP Cities):** 55  

Each waypoint includes:
- Identifier (IDENT)  
- Latitude  
- Longitude  

---

## Task Description

You are required to replicate the same routing optimization scenario using a **Memetic Genetic Algorithm (Memetic GA)**, based on the behavior of the existing codebase.

---

## Requirements

### 1. Algorithm Design

Develop a complete **Memetic Genetic Algorithm** that solves the Traveling Salesman Problem (TSP).

The algorithm must include:

- Population initialization  
- Fitness evaluation (based on total route distance)  
- Selection mechanism  
- Crossover operator  
- Mutation operator  
- Local search (memetic improvement, e.g., hill climbing)  
- Termination condition  

---

### 2. Distance Computation

Use the **Haversine Formula** to compute distances between waypoints.

#### Constants:
- Earth radius: `R = 6,371 km`

#### Variables:
- `ϕ1, ϕ2` → Latitudes (in radians)  
- `λ1, λ2` → Longitudes (in radians)  

> Ensure all latitude and longitude values are converted to radians before computation.

---

### 3. Code Component Breakdown

Clearly define and describe the following components in your implementation:

- Initialization function (e.g., random route generation)  
- Fitness function (route distance calculation)  
- Selection method  
- Crossover function  
- Mutation function  
- Local search function (e.g., hill climbing refinement)  
- Helper functions:
  - Route validation  
  - Duplicate removal  
  - Ordering correction  

---

### 4. Implementation Notes

- The solution should **mirror the logic of the existing codebase** where applicable  
- Randomization may be used to simulate wartime unpredictability  
- All generated routes must remain valid throughout execution  

---

## Example Requirement

Include helper logic such as:

- Function to eliminate unordered or invalid routes  
- Iterative improvement steps (e.g., decrement/increment optimization steps)  

---

## Deadline

**April 10, 2026**

---

## Expected Output

- A working **Memetic Genetic Algorithm implementation**  
- Clearly structured and documented code  
- Explanation of each major component  
- Optimized route satisfying all objectives  

---