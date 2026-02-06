CADI-Framework: Manifold Analysis for Spinal Dynamics
This repository implements the Clinical Advanced Dynamic Index (CADI), a research framework designed to evaluate and predict spinal organizational stability. 
By utilizing biomechanical manifold mapping, the framework transitions from raw kinematic data to a quantified stability index, bridging the gap between clinical observation and deterministic modeling.

Methodology Overview
The core of the framework is based on Support Vector Regression (SVR) with a Radial Basis Function (RBF) kernel. This approach was selected to capture the non-linear "phase transitions" inherent in biological systems, where spinal stability often follows complex, non-linear trajectories rather than simple linear correlations.

The model processes a 9-dimensional biomechanical signature for each subject, encompassing geometric metrics (Mean, Range), statistical distributions (Skewness, Kurtosis), and dynamic volatility indicators (RMSSD).

Empirical Performance

The framework has been validated on a clinical dataset of 253 samples using a strict GroupKFold (subject-independent) cross-validation strategy. This ensures that the predictive power of the model generalizes to unseen patients, a critical requirement for clinical diagnostic tools.
Predictive Fidelity (R^2): 0.71
Spearman Correlation (ρ): 0.84

Technical Components

Mechanistic Simulation: 
Grounded in Spectral Graph Theory, utilizing the second smallest eigenvalue (Algebraic Connectivity) of the Laplacian matrix to generate stability ground-truth labels.

Feature Integration: 
Includes movement volatility (RMSSD) and signal asymmetry (Skewness) as primary drivers of spinal coherence.

Validation Suite: 
Built-in tools for assessing feature impact (Permutation Importance) and data sufficiency (Learning Curves).
