# China Building Heights Benchmark

## Overview

This repository contains benchmarking analysis comparing various open global building footprint datasets with height attributes, with a focus on performance evaluation using manually curated reference data from China.

The benchmark evaluates multiple datasets including:
- **GlobalBuildingAtlas (GAB)** - Currently the best open global dataset of building footprints with heights
- **3D-GloBFP** - Global 3D building dataset
- **Mapflow custom model** - Custom height estimation model
- Legacy China-only datasets

## Key Findings

### GlobalBuildingAtlas (GAB) Performance
- **Best Overall Performance**: GAB significantly outperforms earlier open datasets on our China benchmark
- **Strong Consistency**: Despite using 3 m resolution PlanetScope imagery, GAB demonstrates strong internal consistency
- **Superior Correlation**: Shows higher correlation with manually curated reference data compared to alternative datasets

### 3D-GloBFP Analysis
- Performs better than older China-only datasets
- Suffers from temporal lag issues
- Exhibits noticeable inconsistencies in fast-growing urban areas

### Height Estimation Challenges
- **Tall Building Errors**: Height estimation errors increase sharply for tall buildings
- **Systematic Underestimation**: Clear pattern of underestimation above ~50 m height
- This pattern is shared by most regression-based approaches

### Mapflow Custom Model
- Demonstrates better performance on this benchmark
- Comparison is not fully fair due to:
  - Differences in image resolution
  - Differences in metadata usage

## Repository Structure

```
Cnina_building_hieghts/
├── README.md
├── BuildingH_testing_benchmark_CN.ipynb  # Main analysis notebook
└── data/
    ├── benchmark-all-layers_metrics.csv  # Evaluation metrics
    └── benchmark-all-layers.csv          # Raw benchmark results
```

## Analysis Notebook

The Jupyter notebook `BuildingH_testing_benchmark_CN.ipynb` contains the complete benchmark analysis including:
- Data loading and preprocessing
- Statistical comparisons between datasets
- Visualization of results
- Error analysis and performance metrics

## QGIS Visualization Project

**A complete QGIS project is available** for interactive visualization and interpretation of all benchmark data, including the original imagery used for analysis. This project enables:
- Visual comparison of different datasets
- Spatial analysis of height estimation errors
- Inspection of individual building footprints
- Overlay with reference imagery

Please contact the repository maintainers for access to the QGIS project files.

## Data

The `data/` directory contains:
- **benchmark-all-layers.csv**: Complete benchmark results across all evaluated datasets
- **benchmark-all-layers_metrics.csv**: Computed performance metrics and statistical measures

## Reproducibility

All benchmarks, notebooks, and visualization projects are publicly available to support:
- **Transparency**: Open methodology and data processing steps
- **Reproducibility**: All analysis can be independently verified
- **Further Research**: Foundation for additional comparative studies

## Usage

To run the analysis notebook:

```bash
jupyter notebook BuildingH_testing_benchmark_CN.ipynb
```

Or open directly in VS Code, JupyterLab, or your preferred notebook environment.

## Citation

If you use this benchmark in your research, please cite accordingly and reference the specific datasets evaluated:
- GlobalBuildingAtlas (GAB)
- 3D-GloBFP
- Original data sources

## Contributing

Contributions to improve the benchmark methodology or expand the analysis are welcome. Please open an issue or pull request.

## License

Please refer to individual dataset licenses for usage restrictions. This benchmark analysis is provided for research and educational purposes.
