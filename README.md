# Benchmarking Nanobody Structure Prediction and Downstream Antigen Docking

This repository contains computational work completed during my Summer Research Internship at the Center for Informatics Science (CIS), Nile University.

The project investigates AI-based nanobody (VHH) structure prediction and asks whether differences in structural accuracy, particularly within the CDR-H3 loop, translate into differences in downstream antigen docking and epitope recovery.

## Research Question

Can a general-purpose protein structure predictor compete with antibody- and nanobody-specialized models, and do differences in CDR-H3 structural accuracy affect downstream docking and epitope identification?

## Models Compared

- SimpleFold
- IgFold
- NanoBodyBuilder2 / ImmuneBuilder

## Downstream Case Study

A controlled re-docking experiment was performed using the D7 nanobody–HIV-1 gp120 complex (PDB: 7R73).

The experimental gp120 structure was held fixed while four VHH structures were evaluated:

- Experimental D7 VHH
- SimpleFold prediction
- IgFold prediction
- NanoBodyBuilder2 prediction

Docking was performed using HDOCK, and resulting poses were evaluated using DockQ and epitope-recovery metrics.

## Repository Contents

- `notebooks/.ipynb` — structure preparation and docking workflow
- `report/` — internship technical report
- `figures/` — workflow and result figures
- `data/` — instructions for obtaining public structural data
- `results/` — selected derived outputs and result summaries

## Main Findings

Across the common benchmark of 588 VHH structures, NanoBodyBuilder2 achieved the lowest median CDR-H3 RMSD, while all three models showed similar framework accuracy.

In the 7R73 docking pilot, NanoBodyBuilder2 was the only predicted VHH structure to produce a near-native Top-1 docking pose and recovered 20 of the 26 experimentally observed gp120 epitope residues.

These results suggest that CDR-H3 accuracy may influence downstream antigen docking and epitope recovery, although broader validation across additional complexes is required.

## Tools

Python, PyTorch, SimpleFold, IgFold, ImmuneBuilder/NanoBodyBuilder2, PDBFixer, OpenMM, HDOCK, DockQ, NumPy, Matplotlib

## Data Sources

Experimental structures were obtained from:

- SAbDab / SAbDab2
- RCSB Protein Data Bank

The 7R73 experimental complex can be obtained directly from the RCSB PDB.

## Publication

A manuscript based on this work has been submitted for peer review.

## Acknowledgements

This work was conducted during the Nile University Summer Research Internship at the Center for Informatics Science (CIS), under the supervision of Prof. Mai S. Mabrouk.
