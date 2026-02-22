# GaussianGrasper-3D-Language-Gaussian-Splatting-for-Open-vocabulary-Robotic-Grasping
Implementation and extensions of GaussianGrasper: 3D Gaussian Splatting for language-guided robotic grasping, with improved data calibration, COLMAP hand–eye alignment, and force-closure grasp filtering.


GaussianGrasper Implementation & Refinements
>
> This repository contains our implementation and extensions of GaussianGrasper [2]—a framework for language-guided robotic manipulation using 3D Gaussian Splatting. We address practical limitations of the original pipeline (missing calibration, fragmented reconstructions, misaligned grasps) by introducing a refined workflow from data collection to simulation.
>
> Highlights:
> - Data & calibration: Multi-view RGB-D capture, COLMAP hand–eye calibration, point-cloud generation, and MobileSAM boundary masks.
> - Reconstruction: Gaussian field initialization, Efficient Feature Distillation (EFD), and PCA-based heatmaps for object segmentation.
> - Query & grasp: Open-vocabulary object localization (CLIP), segmentation heatmaps, force-closure filtering of grasp poses, and robotic simulation with reduced angular error.
>
> Experiments use the original data_collection/scene_data dataset plus example_data and custom scenes (kitchen_data/bulldozer, feat_data/garden_table) to validate reconstruction quality, query accuracy, and grasp simulation on static and dynamic scenes.
