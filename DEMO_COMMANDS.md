# CosmicSolver Demo Commands

Here are the commands to run the demonstration for PBLUP, GBLUP, and SSGBLUP using the provided example datasets (both CHIP and WGS panels).
All commands use the optimized AI-REML algorithm for variance component estimation.

## 1. PBLUP (Pedigree-based BLUP)
```powershell
.\cosmicsolver.exe --single-trait --ped example/clean.ped.txt --pheno example/clean.phe.txt --pheno-pos 10 --dcovar 2,3,4,5 --qcovar 7 --vce --vce-mode ai --threads 1 --out results/pblup_cosmicsolver
```

## 2. GBLUP (Genomic BLUP)

**Using Standard CHIP Array (23K SNPs):**
```powershell
.\cosmicsolver.exe --single-trait --bfile example/clean.chip --pheno example/clean.phe.txt --pheno-pos 10 --dcovar 2,3,4,5 --qcovar 7 --vce --vce-mode ai --threads 1 --out results/gblup.chip_cosmicsolver
```

**Using Whole Genome Sequencing (WGS) Data (~9M SNPs):**
```powershell
.\cosmicsolver.exe --single-trait --bfile example/clean.wgs --pheno example/clean.phe.txt --pheno-pos 10 --dcovar 2,3,4,5 --qcovar 7 --vce --vce-mode ai --threads 1 --out results/gblup.wgs_cosmicsolver
```

## 3. SSGBLUP (Single-Step Genomic BLUP)

**Using Standard CHIP Array (23K SNPs):**
```powershell
.\cosmicsolver.exe --single-trait --ped example/clean.ped.txt --bfile example/clean.chip --pheno example/clean.phe.txt --pheno-pos 10 --dcovar 2,3,4,5 --qcovar 7 --vce --vce-mode ai --threads 1 --out results/ssgblup.chip_cosmicsolver
```

**Using Whole Genome Sequencing (WGS) Data (~9M SNPs):**
```powershell
.\cosmicsolver.exe --single-trait --ped example/clean.ped.txt --bfile example/clean.wgs --pheno example/clean.phe.txt --pheno-pos 10 --dcovar 2,3,4,5 --qcovar 7 --vce --vce-mode ai --threads 1 --out results/ssgblup.wgs_cosmicsolver
```
