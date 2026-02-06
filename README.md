CADI-Framework: Urban Manifold Analysis for Swarm Stability
CADI (Chaos-Aware Design Index) is a high-fidelity diagnostic framework designed to evaluate and predict the organizational stability of autonomous swarms within complex urban environments. It maps urban morphological signatures to collective stability indicators using ensemble learning.

Validated on 17,692 urban polygons (Singapore & Boston), the framework identifies a dominant deterministic link between city geometry and swarm order.

Predictive Fidelity (R^2)=0.9136 Superior predictive power
Spearman Correlation (ρ)=0.9558 High rank-order stability
Statistical Significance=p < 0.001 Deterministic link confirmed
Dataset Scale= 17,692 Polygons High statistical power

Technical Stack
Model: Random Forest (RF) Ensemble Regressor (100 estimators).
Sampling: Latin Hypercube Sampling (LHS) for optimized manifold coverage (N=300).
Validation: Scene-independent GroupKFold (cross-city generalization).
Ground Truth: Spectral Graph Theory via Algebraic Connectivity (λ2).

Geometric Features (Xpoly)
The framework processes a 5-dimensional signature for each urban polygon:
Area & Node Density
Boundary Complexity (ln(|V|+1))
Aspect Ratio (Spatial constraint)
Convexity Proxy (Structural irregularity)

Sensitivity
Feature Importance: Identifies Convexity and Node Count as the primary drivers of stability
Weight Invariance: CADI rankings remain >97% consistent under weight perturbations (JRC Standards)
Geographic Generalization: Zero-shot reliability across disparate urban layouts
