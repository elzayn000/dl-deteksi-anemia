# Results directory

This directory accompanies the 14 November 2026 results refresh.

## Consolidated download

[Download the full compact result package](releases/experiment_results_2026-11-14.zip). The archive contains the latest CSV outputs, manuscript Tables I–XI, dataset-cleaning JSON summaries, and Supplementary Tables S1–S3.

The following four large audit/feature artifacts are intentionally excluded from the compact package: `audit_typo_lengkap.csv`, `daftar_rename_typo.csv`, `daftar_rename_typo_FIXED.csv`, and `fitur_ablasi.csv`. They are detailed internal artifacts rather than reader-facing result tables.

## Contents of the package

- Palm classical-ML and CNN baselines.
- Author-modified CNN results and epoch-wise training histories.
- Single-site and pooled model outputs.
- Protocol-replication and robustness results.
- Segmentation, normalization, and sensitivity ablation results.
- Fairness subgroup metrics for ITA and within-site L* terciles.
- Manuscript table exports I–XI.
- Supplementary Tables S1–S3.

The final experiment dataset contains 1,563 images: Palm 520, Nail 528, and Conjunctiva 515. The manuscript also documents an intermediate cleaned set of 1,567 images before four Nail images were removed during the final leakage audit.

Raw pediatric image files are not distributed in this repository.
