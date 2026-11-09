# Results directory

This directory stores computational outputs and manuscript-aligned table exports.

## Manuscript-aligned tables

The CSV files below transcribe the values shown in the manuscript draft uploaded on 9 November 2026. They are intended as reader-facing copies of Tables I–IX:

| Manuscript table | File |
|---|---|
| Table I — dataset distribution | [table_i_dataset_distribution.csv](csv/table_i_dataset_distribution.csv) |
| Table II — selected Palm baselines | [table_ii_selected_baselines.csv](csv/table_ii_selected_baselines.csv) |
| Table III — protocol replication | [table_iii_protocol_replication.csv](csv/table_iii_protocol_replication.csv) |
| Table IV — single-site and pooled models | [table_iv_single_site_pooling.csv](csv/table_iv_single_site_pooling.csv) |
| Table V — ablation summary | [table_v_ablation_reported.csv](csv/table_v_ablation_reported.csv) |
| Table VI — image-brightness groups | [table_vi_brightness_groups.csv](csv/table_vi_brightness_groups.csv) |
| Table VII — signed brightness contrasts | [table_vii_brightness_contrasts.csv](csv/table_vii_brightness_contrasts.csv) |
| Table VIII — robustness (80:20) | [table_viii_robustness_80_20.csv](csv/table_viii_robustness_80_20.csv) |
| Table IX — confusion matrices | [table_ix_confusion_matrices.csv](csv/table_ix_confusion_matrices.csv) |

These table exports are direct transcriptions of the manuscript, not freshly rerun experiments. The source manuscript remains the authority for any editorial interpretation.

## Computational CSV outputs

The csv/ directory also contains detailed notebook outputs, including dataset audit, baseline metrics, pooling, protocol replication, ablation, fairness, robustness, CNN history, and feature-level outputs. See the notebook index for the source notebook of each output.

The initial baseline CSV from Notebook 20 is preserved as baseline_palm_data_bersih_computational_run.csv. The manuscript-facing baseline_palm_data_bersih.csv and supplementary Table S1 use the Stacking accuracy/AUC values reported in the draft. As the draft does not report Stacking confusion counts and all derived metrics, those fields are intentionally blank. Do not infer them from the earlier saved run.

## Statistical corrections

- ablasi_cv_perbandingan.csv retains the Nadeau–Bengio corrected paired-test p-values and adds p_holm_11_kontras_auc for the family of 11 AUC contrasts with site_id.
- fairness_cv_oof_selisih.csv retains raw within-site permutation p-values and adds Bonferroni-adjusted columns for the 12 tests (six groupings/features × two metrics).

The corresponding notebook code now generates these correction columns when rerun.

## Figures

- figures/confusion_matrix/: saved confusion-matrix figures from selected experiment notebook runs.
- figures/training-curves/: saved CNN training-history plots.
- The repository does not currently contain a verified final export for each manuscript Figure 1–6. See figures/README.md for the current inventory and limitations.
