---
description: Biomechanics and AI pipeline for LCA functional assessment prediction.
---

# biomech-ai-pipeline

This skill assists in the development of the ML/CV pipeline for the ACL project.

## Feature Engineering (5 Blocks)
1. **Spatio-temporal (2D)**: Total distance, avg/max velocity, %movement.
2. **2D Projected**: Dynamic Knee Valgus (DKV), FPPA, pelvic tilt, ankle inversion/eversion, ground contact time (GCT), flight time.
3. **3D Joint & CoM**: Knee abduction/valgo, internal rotation, hip flex/add/rot, ankle dorsiflexion, CoM vertical velocity/displacement, XCoM.
4. **Vector Coding**: Hip-Knee and Knee-Ankle coupling angles, coupling variability.
5. **Normalized Temporal**: Time to peak knee flexion/valgo, Fatigue Index.

## ML Implementation Patterns
- **Preprocessing**: `StandardScaler`, `GridSearchCV` for hyperparameter tuning.
- **Models**:
  - `XGBClassifier`
  - `RandomForestClassifier`
  - `SVC` (SVM)
  - `MLPClassifier`
- **Validation**: `StratifiedKFold` with 30 repetitions.

## CV Patterns
- **MediaPipe Pose**: Using 20 landmarks (nose, shoulders, elbows, wrists, hips, knees, ankles, heels, toes).
- **3D-DLT**: Reconstruction from 2D coordinates of multiple cameras.
