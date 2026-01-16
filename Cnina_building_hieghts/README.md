# China Building Heights Benchmark

## Overview

This repository contains benchmarking analysis comparing various open global building footprint datasets with height attributes, with a focus on performance evaluation using manually curated mapping labels for China buildings.

The benchmark evaluates multiple datasets including:
- **GlobalBuildingAtlas (GAB)** - Currently the best open global dataset of building footprints with heights
- **3D-GloBFP** - Global 3D building dataset
- **Mapflow custom model** - Custom height estimation model

## Key Findings

### GlobalBuildingAtlas (GAB) Performance
- **Best Overall Performance**: GAB significantly outperforms earlier open datasets on our China benchmark
- Shows higher correlation with manually curated reference data compared to alternative datasets

### Height Estimation Challenges
- **Tall Building Errors**: Height estimation errors increase sharply for tall buildings
- **Systematic Underestimation**: Clear pattern of underestimation above ~50 m height
- This pattern is shared by most regression-based approaches

### Mapflow Custom Model
- Demonstrates better performance on this benchmark
- Comparison is not fully fair due to differences in image resolution

## Repository Structure

```
Cnina_building_hieghts/
├── README.md
├── BuildingH_testing_benchmark_CN.ipynb  # Main analysis notebook
└── data/
    ├── benchmark-all-layers_metrics.csv  # Evaluation metrics
    └── benchmark-all-layers.csv          # Raw benchmark results
```

## Data

The `data/` directory contains:
- **benchmark-all-layers.csv**: Complete benchmark results across all evaluated datasets
- **benchmark-all-layers_metrics.csv**: Computed performance metrics and statistical measures
- **test-GAB-QGIS-project.zip**: A complete QGIS project is available for interactive visualization and interpretation of all benchmark data, including the original imagery used for analysis.

