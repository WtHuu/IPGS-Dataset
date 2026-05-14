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
│
├── room1.zip
└── room2.zip
