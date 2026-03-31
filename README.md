# CosmicSolver

CosmicSolver is a high-performance Genomic Selection (GS) and Variance Component Estimation (VCE) tool designed for large-scale genetic evaluation and prediction.

## Features
- **High-Performance Exact LMM & AI-REML**: Unified variance component estimation architecture for exact LMM, AI-REML, and stochastic trace estimation for biobank-scale data.
- **Multivariate & RRM Support**: Advanced multi-trait models and Random Regression Models (RRM) utilizing Legendre polynomials.
- **SSGBLUP & Inbreeding Management**: Implements exact inbreeding coefficients (Henderson/Meuwissen & Luo algorithm) for precise A matrix inversion and G matrix alignment.
- **Direct Breeding Value Output**: The generated `.rand` files directly represent breeding values (predictive modules) for individuals.

## Getting Started

### Installation
CosmicSolver is distributed as a pre-compiled executable. No installation or compilation is required. Just download the `cosmicsolver.exe` binary.

### Example Usage
We provide example datasets in the `example/` directory, including both standard CHIP arrays (23K SNPs) and high-density Whole Genome Sequencing (WGS, ~9M SNPs) data. You can find detailed run commands for PBLUP, GBLUP, and SSGBLUP in the `DEMO_COMMANDS.md` file.

You can run a quick test using the following command:

```bash
# Example: Running Single-Step Genomic BLUP (SSGBLUP) evaluation
./cosmicsolver.exe --single-trait --ped example/clean.ped.txt --bfile example/clean.chip --pheno example/clean.phe.txt --pheno-pos 10 --vce --vce-mode ai --out results/ssgblup.chip_cosmicsolver
```

For pre-computed benchmark results comparing different models and datasets, please refer to the `results/` directory.

## Citation
If you use CosmicSolver in your research, please cite our upcoming paper (Details to be updated).

## License
This software is provided for academic and non-commercial research purposes only. Please refer to the `LICENSE` file for more details.
