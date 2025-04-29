# PointNet-based 3D Point Cloud Semantic Segmentation

This project implements a custom **PointNet**-based deep learning pipeline for **semantic segmentation of 3D point clouds**, using the **SemanticKITTI** dataset as the benchmark.  
The architecture leverages both **local** and **global** point features, and extends PointNet with a **T-Net** transformation network for improved invariance to geometric transformations.

---

## 📂 Project Structure

- **Problem1.py**  
  Core deep learning modules:
  - `PointLoader`: Dataset class for loading and preprocessing point clouds and labels.
  - `PointNetEncoder`: Encoder network for feature extraction.
  - `PointNetModule`: Combines local and global features for segmentation.
  - `PointNetFull`: Full model with a transformation network (T-Net).
  - `IoU`: Metric calculation (per-class IoU and mean IoU).

- **utils.py**  
  Utility functions:
  - `seed_torch()`: For reproducibility.
  - `plot_cloud()`: 3D visualization of point clouds with labels.
  - `get_remap_lut()`: Remaps SemanticKITTI labels for training.

- **semantic_kitti.yaml**  
  Contains the label mappings, color codes, and remapping tables for semantic segmentation training.

- **PointNet.ipynb**  
  Jupyter Notebook for training, validation, evaluation, and visualization of model outputs.

---

## 🚀 Features

- Full PyTorch implementation of PointNet for semantic segmentation.
- Dynamic point cloud subsampling for efficient training.
- Global and local feature aggregation with max-pooling.
- Learnable T-Net for input transformation.
- Per-class and mean Intersection-over-Union (IoU) evaluation metrics.
- 3D point cloud visualization using Plotly.

---

## 📦 Setup Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/your_username/PointNet-SemanticSegmentation.git
   cd PointNet-SemanticSegmentation
2. Install the required packages:

    ```bash 
    pip install -r requirements.txt
3. Open `PointNet.ipynb` using VSCode or JupyterLab. Follow the cells to train the model, evaluate on validation data, and visualize results.

