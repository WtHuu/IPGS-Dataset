# IPGS-Dataset

This repository provides the dataset used in the paper:

**IPGS: Inertial-Prior-Guided Surface Gaussian Splatting for Geometry-Consistent Reconstruction of Complex Engineering Environments**

The released data are intended to support research on geometry-consistent scene reconstruction, RGB-D-based reconstruction, Gaussian Splatting, and engineering scene modeling under challenging perceptual conditions, such as weak texture, low illumination, and repetitive texture.

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
└── room2/
    ├── color/
    │   ├── 0000.png
    │   ├── 0001.png
    │   └── ...
    ├── depth/
    │   ├── 0000.png
    │   ├── 0001.png
    │   └── ...
    ├── normal/
    │   ├── 0000.npy
    │   ├── 0000.png
    │   └── ...
    ├── intrinsic/
    │   ├── intrinsic_color.txt
    │   ├── extrinsic_color.txt
    │   ├── intrinsic_depth.txt
    │   └── extrinsic_depth.txt
    └── points3D_rgbd_init.ply
```

### File Description

| Folder / File | Description |
|---|---|
| `color/` | RGB image sequence |
| `depth/` | Depth image sequence |
| `normal/` | Surface normal maps, including `.npy` files and visualization `.png` files |
| `intrinsic/` | Camera intrinsic and extrinsic parameter files |
| `points3D_rgbd_init.ply` | Initial RGB-D point cloud generated from the scene |

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
| Rendered RGB, depth, and normal sequences | To be released progressively |
| Camera parameters, trajectories, and rendering methods | To be released progressively |

This release allows users to inspect the original tunnel scene and generate customized rendered data according to their own reconstruction or simulation requirements.

## Usage

This dataset can be used for academic research on:

- RGB-D scene reconstruction
- Gaussian Splatting-based reconstruction
- Geometry-consistent reconstruction
- Surface normal and depth supervision
- Engineering scene modeling
- Tunnel and weak-texture scene reconstruction

The source code of the proposed IPGS method is not included in this repository.

## Citation

If you use this dataset in your research, please cite our paper:

```bibtex
@article{hu2026ipgs,
  title={IPGS: Inertial-Prior-Guided Surface Gaussian Splatting for Geometry-Consistent Reconstruction of Complex Engineering Environments},
  author={Hu, Wentao and Tian, Chenyu and Wen, Long and Ding, Huafeng},
  journal={Advanced Engineering Informatics},
  year={2026},
  note={Under review}
}
```

Citation information will be updated after publication.

## License

This dataset is released for academic research purposes only. Commercial use is not permitted without permission from the authors.

Users are allowed to download, use, and cite this dataset for non-commercial academic research. Redistribution or modification for commercial purposes is not permitted without prior permission from the authors.
