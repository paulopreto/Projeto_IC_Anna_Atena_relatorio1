# AGENTS.md - Anna Leonel IC Project (LCA & Markerless)

## Project Overview
This project applies Machine Learning (ML) and Computer Vision (CV) to estimate functional assessments assigned by specialists to ACL (Anterior Cruciate Ligament) reconstruction patients. Data is captured during the **CUBE Test** (Multiplanar Unipodal Plyometric Test) using a markerless approach.

- **Objective**: Predict expert functional scores (1-5) using kinematic variables.
- **Population**: ACL reconstruction patients (6-8 months post-op).
- **Funding**: FAPESP Fellowship (Project #2025/12112-5).
- **Internationalization**: Planned Research Internship Abroad (BEPE) at the University of North Florida (UNF) starting Dec 2026.
- **Core Technology**: 
  - **Markerless**: MediaPipe via `vailá` framework.
  - **Reconstruction**: 3D-DLT (Direct Linear Transformation).
  - **ML**: Extreme Gradient Boosting (XGBoost), Random Forest, Logistic Regression, KNN, SVM, Gaussian Naive Bayes, Multilayer Perceptron (MLP).
  - **Dataset**: 27 variables organized in 5 blocks (Spatio-temporal, 2D Projected, 3D Joint/CoM, Vector Coding, Normalized Temporal).

## Directory Structure
- `main.tex`: Core LaTeX report.
- `referencias.bib`: Project bibliography.
- `images/`: Figures and diagrams.
- `pdf/`: Compiled reports.
- `../d3_*`: Directory containing data for different test conditions (R_h, R_ah, L_h, L_ah).

## Technical Protocol
### CUBE Test
- **Dimensions**: 1.35m x 1.35m square (3x3 grid of 0.45m squares).
- **Execution**: Single-leg jumps in clockwise (CW) and counter-clockwise (CCW) directions for both legs.
- **Trial Naming**: `R_h` (Right Clockwise), `R_ah` (Right Counter-Clockwise), `L_h` (Left Clockwise), `L_ah` (Left Counter-Clockwise).

### ML Pipeline
1. **Pose Estimation**: 20 landmarks from MediaPipe.
2. **Filtering**: 4th order Butterworth filter.
3. **Reconstruction**: 3D-DLT with 9 static markers calibration.
4. **Validation**: 30x repeated Stratified K-Fold cross-validation.
5. **Metrics**: Balanced Accuracy, Precision, Recall, F1-Score.

## Ethical and Collaborative Information
- **CAAE**: 89943725.2.0000.5659
- **Advisor**: Prof. Dr. Paulo Roberto Pereira Santiago
- **Collaborators**: 
  - Prof. Dr. Rodrigo Salim (Clinical co-advisor)
  - Rafael Luiz Martins Monteiro (PhD candidate)
  - Prof. Dr. Guilherme Manna Cesar (International Advisor - UNF)
  - Dr. Sherry Pinkstaff (UNF - Department Chair)

## Cursor Skills
- **biomech-ai-pipeline**: Feature engineering and ML model implementation.
- **latex-scientific-report**: LaTeX formatting and scientific writing standards.
- **opensim-automation**: Future expansion (optional) for OpenSim integration.
