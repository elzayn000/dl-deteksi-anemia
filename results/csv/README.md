# CSV result files

This directory contains experiment-level CSV outputs and the compact CSV exports corresponding to manuscript Tables I–XI. Large audit/intermediate files are compressed separately in [`large/README.md`](large/README.md).

## Manuscript-aligned tables

| Table | File | Description |
|---|---|---|
| I | `table_i_dataset_distribution.csv` | Dataset counts by image site and the final experiment set |
| II | `table_ii_selected_baselines.csv` | Selected baseline performance across the reported split schemes |
| III | `table_iii_protocol_replication.csv` | Replication of the augmentation/splitting protocols |
| IV | `table_iv_single_site_pooling.csv` | Single-site versus pooled experiment comparisons |
| V | `table_v_ablation_reported.csv` | Reported ROI-segmentation and color-normalization ablation results |
| VI | `table_vi_brightness_groups.csv` | Metrics by image-brightness grouping |
| VII | `table_vii_brightness_contrasts.csv` | Paired brightness-group contrasts and uncertainty estimates |
| VIII | `table_viii_robustness_80_20.csv` | Robustness results under the 80:20 evaluation scheme |
| IX | `table_ix_confusion_matrices.csv` | Confusion-matrix counts and derived metrics for selected models |
| X | `table_x_empty_mask_counts.csv` | Empty-mask counts by preprocessing treatment and image site |
| XI | `table_xi_sensitivity_analysis.csv` | Sensitivity contrasts for ablation and empty-mask handling |

## Experiment-level outputs

| File pattern / file | Contents |
|---|---|
| `baseline_palm_data_bersih.csv` | Classical-model baseline results on cleaned Palm data |
| `baseline_cnn_palm_data_bersih.csv` | Reference CNN baseline results |
| `varian_cnn_palm_data_bersih.csv` | Author-modified CNN variant results |
| `hasil_eksperimen_konsisten.csv` | Consistent single-site and pooled experiment results |
| `hasil_robustness_konsisten.csv` | Results under image perturbations |
| `replikasi_protokol_paper.csv` | Protocol-replication results |
| `riwayat_pelatihan_cnn.csv`, `riwayat_varian_cnn.csv` | Epoch-level CNN training histories |
| `ablasi_*.csv` | Split-level, cross-validation, additional contrast, and empty-mask ablation outputs |
| `fairness_*.csv` | Brightness-group composition, out-of-fold metrics, and paired fairness contrasts for the two manuscript-reported groupings (merged ITA and within-site L* tertiles) |

## Reading the files

CSV files use header rows. Most metric columns encode percentages in their names (for example, `_pct`). Some compact manuscript exports combine multiple metrics in one cell, as indicated by the column name. Preserve the original values and missing-value markers when importing the files.

The detailed fairness outputs in the original `hasil_revisi_v2` experiment package also contain an exploratory 8-bit brightness grouping (`L < 100`, `100 ≤ L < 150`, and `L ≥ 150`). The branch-level `fairness_*.csv` files intentionally retain only the two groupings reported in the latest manuscript: merged ITA categories and within-site L* tertiles. The omitted 8-bit grouping is exploratory and is not included in manuscript Tables VI–VII.

Files in this directory are research outputs, not raw image datasets. For the complete record of the cleaning process, use `../audit/`; for the detailed compressed typo and feature-level artifacts, use `large/`.
