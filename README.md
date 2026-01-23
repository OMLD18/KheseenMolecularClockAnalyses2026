# Data and Code for Molecular Clock Calibration Sensitivity Analyses

This repository contains input files, configuration files, and outputs for Bayesian molecular clock calibration sensitivity analyses conducted using MCMCTree (PAML package).
All analyses are based on the methods detailed in: E. Carlisle, Z. Yin, D. Pisani, P. C. Donoghue, Ediacaran origin and Ediacaran-Cambrian diversification of Metazoa. *Science Advances* **10**, eadp7161 (2024).

The files provided here enable reproducibility and independent evaluation of the results presented in ...

---

## Repository Organization

Each analysis is contained within a separate directory corresponding to a distinct calibration or model scenario:

File(analysisname)/
- ConcatAlign.phy
- lg.dat
- data/
  - 1PoriMonoXenacoelCarlisle24(analysisname).txt
- mcmc/
  - in.BV
  - mcmctree.ctl
  - out.txt
  - SeedUsed
  - mcmc.txt
  - FigTree.tre

---

## File Descriptions

### Molecular Data

**`ConcatAlign.phy`**

Concatenated molecular alignment in PHYLIP format used for divergence time estimation. The alignment corresponds to the taxon sampling and fixed topology described in *Carlisle et al. (2024)*. Taxon order and names must match those in the tree file.

---

### Phylogenetic and Model Data (`data/`)

**`1PoriMonoXenacoelCarlisle24(analysisname).txt`**  

Fixed topology tree file used by MCMCTree, including:
- Node labels
- Fossil calibration constraints (minimum/maximum bounds, soft priors)
The `analysisname` suffix denotes alternative calibration schemes explored as part of sensitivity analyses.

**`lg.dat`** 

LG amino acid substitution rate matrix used in MCMCTree.

---

### MCMC Configuration and Output (`mcmc/`)

**`mcmctree.ctl`** 

Primary MCMCTree control file specifying:
- Clock model
- Prior distributions on divergence times and substitution rates
- MCMC parameters (burn-in, sampling frequency, chain length)
- Input and output file paths

**`in.BV`** 

Branch-length variance file.

**`MCMC output files`** (`out.txt`, `FigTree.tre`, etc.)

Contain posterior summaries of divergence times, evolutionary rates, and MCMC diagnostics.

---

## Citation

If you use these data or configuration files, please cite:

E. Carlisle, Z. Yin, D. Pisani, P. C. Donoghue, Ediacaran origin and Ediacaran-Cambrian diversification of Metazoa. *Science Advances* **10**, eadp7161 (2024).
XXXX

and the relevant methodological references for PAML and MCMCTree.

---

## Data and Code Availability

All data and configuration files necessary to reproduce the molecular clock calibration sensitivity analyses are available in this repository.
