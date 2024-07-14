# Incremental Multiview Point Cloud Registration

This repository provides the open-source implementation of the "Incremental Multiview Point Cloud Registration".

## Overview

The Incremental Multiview Point Cloud Registration (IncreMVR) is an innovative method designed to progressively align point clouds from multiple views into a unified coordinate system. This approach stands out from traditional global registration schemes by incrementally integrating scans, enhancing both precision and robustness in multiview 3D reconstruction tasks.

## Key Features

- **Incremental Registration Pipeline**: A novel strategy that incrementally aligns scans to construct a cohesive point cloud model.
- **Supports Both Matcher Types**: Compatible with both detector-based and detector-free registration matchers.
- **Benchmark Performance**: Demonstrates superior performance over existing methods on standard datasets such as 3D(Lo)Match, ScanNet, and ETH.

## Installation

To set up the IncreMVR framework, follow these steps:

1. **Clone the Repository**:
   ```shell
   git clone https://github.com/Choyaa/IncreMVR.git
   cd IncreMVR
   ```

2. **Create a Conda Environment** (optional, but recommended):
   ```shell
   conda env create -f environment.yml
   conda activate incremvr
   ```
## Dataset
   
## Configuration

The IncreMVR framework requires a configuration file to set up execution parameters. Sample configuration files are located in the `config` folder. Customize these files according to your specific requirements and dataset paths.

## Usage

The IncreMVR framework follows a structured pipeline for multiview point cloud registration:

### Step 1: Initialization
Set up the initial scan pair and the sparse scan graph.

### Step 2: Incremental Registration
Perform incremental registration of scans based on the scan graph.

### Step 3: Track Refinement (Optional)
Refine the tracks for detector-free methods to enhance accuracy.

### Main Execution
Run the IncreMVR pipeline with:
```shell
python run.py --config_path /path/to/your/config/file
```

## Experiments

Detailed experiments to reproduce results from the paper on benchmark datasets are provided in the `experiments` folder.

## Citation

For academic use, please cite the following paper:
```bibtex
@article{cheng2024incremental,
  title={Incremental Multiview Point Cloud Registration},
  author={Cheng, Xiaoya and Liu, Yu and Zhang, Maojun and Yan, Shen},
  journal={arXiv preprint arXiv:2407.05021},
  year={2024}
}
```
