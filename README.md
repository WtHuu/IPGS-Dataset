# IPGS-Dataset

This repository provides the dataset used in the paper:

**IPGS: Inertial-Prior-Guided Surface Gaussian Splatting for Geometry-Consistent Reconstruction of Complex Engineering Environments**

The released data are intended to support research on geometry-consistent scene reconstruction, RGB-D reconstruction, Gaussian Splatting, and engineering scene modeling under challenging perceptual conditions, such as weak texture, low illumination, and repetitive texture.

> **Note:** This repository only provides dataset documentation and download links. The implementation code of the proposed IPGS method is not included in the current release.

## Dataset Download

The complete dataset files are hosted on Google Drive due to the file-size limitations of GitHub repositories.

[Download IPGS Dataset from Google Drive](https://drive.google.com/drive/folders/19Ss8rekiVo-ZN26NkrknPDeHBpTasUA2?usp=sharing)

## Dataset Overview

The current release contains two parts:

| Dataset | Description | Current Release Status |
|---|---|---|
| DK Dataset | RGB-D data collected using an Azure Kinect DK camera | Released |
| Tunnel Dataset | A tunnel scene constructed in Blender | Raw Blender data released; sampled RGB-D data will be released progressively |

## DK Dataset

The DK dataset currently contains two scenes:

- `room1`
- `room2`

Each scene contains RGB images, depth images, normal maps, camera intrinsic/extrinsic parameters, and an initial RGB-D point cloud.

The structure of the DK dataset is as follows:

```text
DK_data/
├── room1/
│   ├── color/
│   │   ├── 0000.png
│   │   ├── 0001.png
│   │   └── ...
│   ├── depth/
│   │   ├── 0000.png
│   │   ├── 0001.png
│   │   └── ...
│   ├── normal/
│   │   ├── 0000.npy
│   │   ├── 0000.png
│   │   └── ...
│   ├── intrinsic/
│   │   ├── intrinsic_color.txt
│   │   ├── extrinsic_color.txt
│   │   ├── intrinsic_depth.txt
│   │   └── extrinsic_depth.txt
│   └── points3D_rgbd_init.ply
│
├── room2/
│   ├── color/
│   │   ├── 0000.png
│   │   ├── 0001.png
│   │   └── ...
│   ├── depth/
│   │   ├── 0000.png
│   │   ├── 0001.png
│   │   └── ...
│   ├── normal/
│   │   ├── 0000.npy
│   │   ├── 0000.png
│   │   └── ...
│   ├── intrinsic/
│   │   ├── intrinsic_color.txt
│   │   ├── extrinsic_color.txt
│   │   ├── intrinsic_depth.txt
│   │   └── extrinsic_depth.txt
│   └── points3D_rgbd_init.ply


## Tunnel Dataset

In addition to the DK dataset, this release also includes the original Tunnel dataset.

The released Tunnel dataset contains the **raw Blender scene data** used as the original source of our tunnel reconstruction experiments. The Blender scene provides a synthetic tunnel environment with low illumination, repetitive textures, and complex tunnel-like geometric structures, which is designed to simulate challenging engineering conditions commonly encountered in underground or confined environments.

In the current release, the Tunnel dataset is provided in its original Blender format. This raw Blender data serves as the source scene for subsequent image rendering, depth generation, trajectory sampling, and reconstruction experiments.

Please note that the currently released Tunnel data are **not yet the sampled RGB-D image sequences** used directly for training or evaluation. The rendered RGB images, depth maps, camera poses, sampling trajectories, normal maps, and rendering scripts/methods will be released progressively in future updates.

The current release status of the Tunnel dataset is summarized as follows:

| Data Type | Release Status |
|---|---|
| Raw Blender scene data | Released |
| Blender `.blend` scene file | Released |
| Rendered RGB image sequences | To be released progressively |
| Rendered depth image sequences | To be released progressively |
| Camera poses and sampling trajectories | To be released progressively |
| Normal maps and auxiliary data | To be released progressively |
| Rendering scripts and rendering method | To be released progressively |

This release allows users to inspect the original tunnel scene and generate customized rendered data according to their own reconstruction or simulation requirements.
