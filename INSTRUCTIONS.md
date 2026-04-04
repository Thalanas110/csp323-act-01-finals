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
- Start and end at **RPUB (Basa Air Base, Pampanga)** (**but can be made random as again, we assume wartime constraints and realities.**)
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

## PROFESSOR INSTRUCTIOBNS
As discussed in our previous session, you are required to use the template introduced with Adrian as the basis for this activity. This template follows a standard industry workflow in software development, where you first analyze the problem, define the objectives, develop an algorithm or pseudocode, and then translate that algorithm into working code. Your task is to complete and enhance the template accordingly.

The problem statement must remain exactly as provided and should not be modified in any way. You are only allowed to improve the objectives, ensuring that they are clear, specific, and directly aligned with the given problem. You are also required to develop or enhance the algorithm (pseudocode) by presenting a clear, logical, and step-by-step solution.

For the Code Integration section, you must follow a structured format where each step in your algorithm is paired with its corresponding code segment. This means that for every algorithm step, you must show the exact part of the code that implements it. The format should clearly present the algorithm step followed by its corresponding code block. You will use the code provided by Adrian as your base, but you are allowed to modify or improve it as needed, as long as it correctly solves the problem. The mapping between the algorithm and the code must be clear, consistent, and one-to-one.

Your final outputs must include the following: (1) a PDF copy of the completed template with your name and section clearly indicated, and (2) the Jupyter Notebook file (.ipynb) containing your working code. Ensure that all components—objectives, algorithm, and code—are consistent with one another. Any mismatch between the algorithm and the code, lack of clarity, or incomplete sections will affect your evaluation.



