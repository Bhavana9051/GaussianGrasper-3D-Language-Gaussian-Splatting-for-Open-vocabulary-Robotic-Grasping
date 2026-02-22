# GaussianGrasper-3D-Language-Gaussian-Splatting-for-Open-vocabulary-Robotic-Grasping

Implementation and extensions of **GaussianGrasper** [2]: 3D Gaussian Splatting for language-guided robotic grasping, with improved data calibration, COLMAP hand–eye alignment, and force-closure grasp filtering.

---

## Paper

**Research paper:** [Gaussian Graper Paper](https://drive.google.com/file/d/1U0J6eT5NciKtjVC1nruPP3V1ODCdYrEB/view)

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

**Final pipeline**

![Final pipeline](pipeline%20docs/final_flowchart.jpg)

**Redefined pipeline**

![Redefined pipeline](pipeline%20docs/Redefined_Pipeline.jpg)

### Execution recordings

Click each link to view or download the video (GitHub does not embed video in READMEs).

| Description | Video |
|-------------|-------|
| Dataset and heatmaps | [DatasetAndHeatmaps.webm](DatasetAndHeatmaps.webm) |
| Splatting simulation (final) | [splattingSimulation_final.webm](splattingSimulation_final.webm) |
| Training the model | [train.webm](train.webm) |
---

## References

- **Original work:** Zheng et al., [GaussianGrasper for Open-Vocabulary Grasping](https://ieeexplore.ieee.org/stamp/stamp.jsp?arnumber=10607869), IEEE Proceedings, 2024.
