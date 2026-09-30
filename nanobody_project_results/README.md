# Results

This folder contains compact result tables from the nanobody structure-prediction benchmark
and the 7R73A downstream docking/epitope-recovery pilot.

## Files

- `benchmark_summary.csv` — paired structural benchmark summary for SimpleFold, IgFold, and NanoBodyBuilder2.
- `simplefold_sampling_summary.csv` — uncertainty, sampling-coverage, and ESM2-probe results.
- `7R73_top1_docking_epitope.csv` — Top-1 HDOCK/DockQ and epitope-recovery results.
- `7R73_best_top10_docking_epitope.csv` — best-DockQ pose among the Top-10 HDOCK candidates.

## Important interpretation

The structural benchmark used 597 VHH targets overall and 588 targets for direct three-model
paired comparison. The downstream docking analysis is a single controlled pilot using the
D7 nanobody–HIV-1 gp120 complex (PDB 7R73), so the docking/epitope findings should not be
generalized across nanobody–antigen systems without additional validation.
