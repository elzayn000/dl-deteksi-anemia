# Results directory

This folder contains experiment outputs and manuscript-aligned table exports for the 14 November 2026 research revision.

## Manuscript-aligned tables

| Manuscript table | CSV export |
|---|---|
| Table I — dataset distribution | [table_i_dataset_distribution.csv](csv/table_i_dataset_distribution.csv) |
| Table II — selected Palm baselines | [table_ii_selected_baselines.csv](csv/table_ii_selected_baselines.csv) |
| Table III — protocol replication | [table_iii_protocol_replication.csv](csv/table_iii_protocol_replication.csv) |
| Table IV — single-site and pooled models | [table_iv_single_site_pooling.csv](csv/table_iv_single_site_pooling.csv) |
| Table V — ablation and corrected tests | [table_v_ablation_reported.csv](csv/table_v_ablation_reported.csv) |
| Table VI — ITA brightness groups | [table_vi_brightness_groups.csv](csv/table_vi_brightness_groups.csv) |
| Table VII — brightness contrasts | [table_vii_brightness_contrasts.csv](csv/table_vii_brightness_contrasts.csv) |
| Table VIII — robustness (80:20) | [table_viii_robustness_80_20.csv](csv/table_viii_robustness_80_20.csv) |
| Table IX — selected confusion matrices | [table_ix_confusion_matrices.csv](csv/table_ix_confusion_matrices.csv) |
| Table X — empty-mask counts | [table_x_empty_mask_counts.csv](csv/table_x_empty_mask_counts.csv) |
| Table XI — sensitivity analysis | [table_xi_sensitivity_analysis.csv](csv/table_xi_sensitivity_analysis.csv) |

These table CSVs are reader-facing summaries. Detailed current experiment outputs are also available in `csv/`, including Palm/CNN baselines, ablation summaries and contrasts, and fairness subgroup data.

## Supporting figures

The latest seven confusion matrices and two CNN training curves are stored in [supporting_figures_svg_2026-11-14.tar.xz](releases/supporting_figures_svg_2026-11-14.tar.xz). Extract the archive inside `results/figures/` to restore their folders.

## Final data and interpretation

The final experiment dataset contains 1,563 images: Palm 520, Nail 528, and Conjunctiva 515. The manuscript also records the intermediate cleaned collection of 1,567 images before four Nail images were excluded in the final leakage audit. The revised fairness analysis retains ITA and within-site L* tercile groups; the legacy 8-bit L* grouping is excluded.
