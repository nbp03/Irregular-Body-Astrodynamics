# Irregular Body Gravitational Modeling & V&V Suite

**Overview:** A computational astrodynamics framework developed in MATLAB to model simplified gravitational potential models against high-fidelity polyhedron truth models for irregular, elongated celestial bodies (such as asteroids and small moons).

![Error Contour Plot Placeholder](link-to-your-contour-plot.png)

## 1. Research Objective & The Systems Engineering Problem
High-fidelity polyhedron gravity models provide exact potential and acceleration solutions around irregular bodies, but their extreme computational cost makes them impractical for real-time onboard autonomous navigation and long-term orbit propagation. 

This project evaluates computationally efficient surrogates—including **Double-Segment**, **Mascon/Dipole**, and **Structure-Preserving Hamiltonian** models—to define exact spatial accuracy limits and computational speedups relative to polyhedron benchmarks.

**High-Performance Parallel Computing (HPC):** Engineered parallelized MATLAB execution scripts (`parfor` / batch jobs) deployed on Embry-Riddle’s **Vega Supercomputing Cluster** via SSH and SFTP protocols, reducing full-grid polyhedron benchmark runtimes from days to minutes.

![3D Asteroid Mesh Placeholder](link-to-your-asteroid-mesh.png)

## 2. Peer-Reviewed Publications & Conference Presentations
The codebase and validation frameworks in this repository directly support three co-authored papers accepted for presentation in 2026:

1. *"Comparative Analysis of Simplified Gravitational Models for Irregular Elongated Bodies,"* Oral Presentation at the **2026 Astrodynamics Specialist Conference**, Whistler, BC, Canada, July 26–30, 2026.
2. *"Developing a Structure-Preserving Hamiltonian Surrogate for Dynamics Around Irregular Bodies,"* Oral Presentation at the **2026 Astrodynamics Specialist Conference**, Whistler, BC, Canada, July 26–30, 2026.
3. *"Modeling and Validating the Gravitational Potential of Irregular Asteroids Using a Double-Segment Approach,"* Oral Presentation at **2026 ASCEND**, Washington, D.C., USA, May 19–21, 2026.

## 3. Repository Structure
* `/models` — Core MATLAB functions for the Polyhedron benchmark, Double-Segment approach, and simplified surrogate potentials.
* `/hpc_cluster` — Batch submission scripts and parallel pool configurations for the Vega supercomputer.
* `/plotting` — Scripts for generating error contour heatmaps and 3D surface mesh visualizations.
* `/sample_data` — Sample asteroid shape models (`.obj` / `.tab` vertices and facets) and validation output matrices.

## 4. Usage & Dependencies
* **Environment:** MATLAB R2025b+
* **Required Toolboxes:** Parallel Computing Toolbox (for multi-core/cluster execution).
