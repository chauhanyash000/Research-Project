# Modelling the Behaviour of Shape Memory Materials Using Machine Learning Approaches

> A supervised learning approach to Shape Memory Alloy (SMA) parameter characterisation using Artificial Neural Networks.

---

## Overview

Shape Memory Alloys (SMAs) are stimuli-responsive smart materials capable of large recoverable deformation under external stimuli such as heat, electricity, light, or magnetism. Despite their vast potential across engineering domains, widespread adoption is hindered by the complexity of characterising their hysteretic, non-linear, thermo-mechanical behaviour.

This research reviews and assesses machine learning — specifically Artificial Neural Networks (ANNs) — as a faster, data-efficient alternative to traditional SMA parameter characterisation methods.

---

## The Problem

Traditional SMA characterisation:
- Requires extensive experimental data collection
- Demands deep domain expertise
- Is time-consuming and resource-intensive

Existing constitutive models are accurate but depend on prior knowledge of material parameters — making entry into SMA application difficult.

---

## The Approach

A **supervised learning ANN** is trained to identify key SMA material parameters directly from strain-temperature hysteresis data:

| Input | Output |
|-------|--------|
| Strain-temperature hysteresis coordinates | Transformation temperatures |
| | Stress influence coefficients |

Training data is generated computationally using a constitutive SMA model — eliminating the need for large experimental datasets.

---

## Applications of SMAs

**Aerospace**
- Variable geometry chevrons (Boeing)
- Wing morphing with SMA actuators

**Biomedical**
- Orthodontic wires, stents, surgical tools

**Engineering & MEMS**
- Micro-scale actuators
- Laser-actuated NiTi bimorphs

---

## Numerical Methods Reviewed

Two return mapping algorithms for SMA thermo-mechanical model implementation:

| Algorithm | Convergence | Stability | Complexity |
|-----------|-------------|-----------|------------|
| Closest Point Projection (Backward Euler) | Quadratic, guaranteed | Unconditionally stable | High — 6×6 tensor inversion |
| Convex Cutting Plane (Forward Euler) | Quadratic, not guaranteed | Stable for forward transformation only | Lower, simpler |

---

## Results

The ANN model, trained on **428 specimens** via the Taguchi method, achieved:

- **87%** accuracy for transformation temperature identification
- **73%** accuracy for stress influence coefficient identification
- Outperformed a baseline ANN trained on 10× more data (4,296 specimens)

Once trained, the model identifies SMA parameters from hysteresis data alone — faster and with less expertise than existing methods.

---

## Future Directions

1. Build and train an original supervised ML model from the ground up
2. Generate training data and implement the model pipeline
3. Tune hyperparameters and improve accuracy
4. Explore hybrid machine learning approaches for characterisation

---

## Key References

- Henrickson, Kirkpatrick & Valasek (2013) — *Characterization of Shape Memory Alloys using Artificial Neural Networks*, AIAA Aerospace Sciences Meeting
- Qidwai, Hartl & Lagoudas (2008) — *Numerical Implementation of an SMA Thermomechanical Constitutive Model using Return Mapping Algorithms*, Springer
- Sofla et al. (2010) — *Shape Morphing of Aircraft Wing: Status and Challenges*, Materials & Design
- Buehler, Gilfrich & Wiley (1963) — *Effect of Low-Temperature Phase Changes on Mechanical Properties of Alloys near Composition TiNi*, Journal of Applied Physics

---

## License

[MIT License](LICENSE)
