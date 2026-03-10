---
description: OpenSim automation for markerless biomechanical analysis.
---

# opensim-automation

Assists in integrating the markerless output with OpenSim.

## Pose2Sim Implementation
- Convert `MediaPipe` landmarks to `.trc` format.
- Run `Pose2Sim` for 3D reconstruction and OpenSim-ready scaling.

## Muscle Groups for SO (Static Optimization)
- **Hip**: gluteus medius/minimus, gluteus maximus, TFL.
- **Knee**: quadriceps (rectus femoris, vastus medialis/lateralis/intermedius), hamstrings.
- **Plantarflexors**: gastrocnemius, soleus.

## Dynamic Output Variables
- Knee abduction/adduction moment (N·m/kg).
- Joint power (W/kg).
- Muscle forces (N) and activations (0-1).
