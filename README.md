CADI (Chaos-Aware Design Index) is a high-fidelity diagnostic framework designed to evaluate and predict the organizational stability of autonomous swarms within complex urban environments.

By utilizing urban morphological manifold mapping, the framework transitions from raw spatial geometry (polygons) to a quantified stability index, bridging the gap between urban network topology and deterministic swarm dynamics.

Empirical Performance (nuScenes Validation)
The framework has been validated using the nuScenes Map Expansion (v1.3) dataset, encompassing a massive scale of urban data. Unlike traditional small-scale studies, CADI identifies a dominant deterministic signal even within high-entropy urban substrates.

Dataset Scale: 17,692 Urban Polygons (Singapore & Boston)
Predictive Fidelity (R^2): 0.7356S
tatistical Significance: p < 0.001
Validation Strategy:GroupKFold (Scene-independent validation across different geographic cities)

Methodology Overview
The core of the framework is based on Support Vector Regression (SVR) with a Radial Basis Function (RBF) kernel. This approach was selected to capture the non-linear "phase transitions" inherent in collective systems, where swarm stability follows complex trajectories dictated by the geometric constraints of the city.

Technical Components:
Mechanistic Simulation: 
Grounded in Spectral Graph Theory, utilizing the second smallest eigenvalue (Algebraic Connectivity, λ2) of the Laplacian matrix to generate stability ground-truth labels.

Urban Feature Integration: 
The model processes a 5-dimensional geometric signature for each urban polygon:
Area & Node DensityBoundary Complexity (ln(|V|+1))
Aspect Ratio (Spatial Constraint)
Convexity Proxy (Structural Irregularity)

Validation Suite
The repository includes built-in scientific tools for ensuring model robustness:

Permutation Importance: Ranks urban features by their impact on swarm stability (identifying Area and Node Count as primary drivers)

Learning Curves: Mathematically proves data sufficiency and model convergence across the 17692 sample manifold

Geographic Invariance: Proves the CADI index remains consistent across disparate urban layouts (Singapore vs Boston)
