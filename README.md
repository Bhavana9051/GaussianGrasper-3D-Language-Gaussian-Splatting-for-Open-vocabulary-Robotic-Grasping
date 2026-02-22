# GaussianGrasper-3D-Language-Gaussian-Splatting-for-Open-vocabulary-Robotic-Grasping

Implementation and extensions of **GaussianGrasper** [2]: 3D Gaussian Splatting for language-guided robotic grasping, with improved data calibration, COLMAP hand–eye alignment, and force-closure grasp filtering.

---

## Paper

**Research paper:** [majorProject_8thSem.pdf](https://drive.google.com/file/d/1U0J6eT5NciKtjVC1nruPP3V1ODCdYrEB/view)

---

## Overview

This repository contains our implementation and extensions of **GaussianGrasper** [2]—a framework for language-guided robotic manipulation using 3D Gaussian Splatting. We address practical limitations of the original pipeline (missing calibration, fragmented reconstructions, misaligned grasps) by introducing a refined workflow from data collection to simulation.

**Highlights:**
- **Data & calibration:** Multi-view RGB-D capture, COLMAP hand–eye calibration, point-cloud generation, and MobileSAM boundary masks.
- **Reconstruction:** Gaussian field initialization, Efficient Feature Distillation (EFD), and PCA-based heatmaps for object segmentation.
- **Query & grasp:** Open-vocabulary object localization (CLIP), segmentation heatmaps, force-closure filtering of grasp poses, and robotic simulation with reduced angular error.

Experiments use the original `data_collection/scene_data` dataset plus `example_data` and custom scenes (`kitchen_data/bulldozer`, `feat_data/garden_table`) to validate reconstruction quality, query accuracy, and grasp simulation on static and dynamic scenes.

---

## Pipeline & Results

### Flowcharts

| Description | Link |
|-------------|------|
| Final pipeline | [final_flowchart.png](https://drive.google.com/file/d/1Rv_2gpI6L-ydxVk8aOVCGXvxgqmiYjlS/view?usp=drive_link) |
| Redefined pipeline | [Redefined_Pipeline.png](https://drive.google.com/file/d/1o27B05nS5hm3deaQXxHPRKqasVU2OMRR/view?usp=drive_link) |

### Execution recordings

| Description | Link |
|-------------|------|
| Dataset and heatmaps | [DatasetAndHeatmaps.webm](https://drive.google.com/file/d/1Ad8Tr0Y9BF1foGgpjqS5a3owd-Ju9_6o/view?usp=drive_link) |
| Splatting simulation (final) | [splattingSimulation_final.webm](https://drive.google.com/file/d/1SysWv01W99xzuMKSFNndvJh1s-5i-Vjm/view?usp=drive_link) |
| Training the model | [training / splatting video](https://drive.google.com/file/d/1SysWv01W99xzuMKSFNndvJh1s-5i-Vjm/view?usp=drive_link) |
---

## References

- **Original work:** Zheng et al., [GaussianGrasper for Open-Vocabulary Grasping](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10607869), IEEE Proceedings, 2024.
