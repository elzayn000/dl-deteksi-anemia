# Results directory

This directory stores the committed computational outputs and manuscript-aligned table exports.

## Manuscript-aligned tables

The CSV files below transcribe the values shown in the manuscript draft uploaded on 9 November 2026. They are reader-facing copies of Tables I–IX:

| Manuscript table | File |
|---|---|
| Table I — dataset distribution | [`table_i_dataset_distribution.csv`](csv/table_i_dataset_distribution.csv) |
| Table II — selected Palm baselines | [`table_ii_selected_baselines.csv`](csv/table_ii_selected_baselines.csv) |
| Table III — protocol replication | [`table_iii_protocol_replication.csv`](csv/table_iii_protocol_replication.csv) |
| Table IV — single-site and pooled models | [`table_iv_single_site_pooling.csv`](csv/table_iv_single_site_pooling.csv) |
| Table V — ablation summary | [`table_v_ablation_reported.csv`](csv/table_v_ablation_reported.csv) |
| Table VI — image-brightness groups | [`table_vi_brightness_groups.csv`](csv/table_vi_brightness_groups.csv) |
| Table VII — signed brightness contrasts | [`table_vii_brightness_contrasts.csv`](csv/table_vii_brightness_contrasts.csv) |
| Table VIII — robustness (80:20) | [`table_viii_robustness_80_20.csv`](csv/table_viii_robustness_80_20.csv) |
| Table IX — confusion matrices | [`table_ix_confusion_matrices.csv`](csv/table_ix_confusion_matrices.csv) |

These table exports are transcriptions of the manuscript draft, not freshly rerun experiments. The source manuscript remains the authority for editorial interpretation.

Table II contains the selected-baseline accuracy and test-AUC values for both 70:10:20 and 80:10:10 schemes. The expanded per-configuration baseline metrics are provided separately in [Supplementary Table S1](../supplementary/Supplementary_Table_S1_Full_Baseline.csv).

## Computational CSV outputs

The `csv/` directory also contains detailed notebook outputs, including dataset audit, classical ML baselines, CNN baselines and variants, pooling, protocol replication, ablation, fairness, robustness, CNN training history, and feature-level outputs. See [`../notebooks/README.md`](../notebooks/README.md) for the source notebook of each output.

The initial baseline CSV from Notebook 20 is preserved as [`baseline_palm_data_bersih_computational_run.csv`](csv/baseline_palm_data_bersih_computational_run.csv). The manuscript-facing [`baseline_palm_data_bersih.csv`](csv/baseline_palm_data_bersih.csv) and Table II export reproduce the selected values shown in the draft. Supplementary Table S1 provides the expanded baseline detail using Appendix A1 of the final experiment report. Stacking accuracy, precision, sensitivity, specificity, F1, test AUC, and validation AUC are taken from that appendix; TP/TN/FP/FN are reconstructed from class supports and rounded sensitivity/specificity. Validation accuracy remains blank because it is not reported.

CNN experiment outputs are available in [`baseline_cnn_palm_data_bersih.csv`](csv/baseline_cnn_palm_data_bersih.csv), [`varian_cnn_palm_data_bersih.csv`](csv/varian_cnn_palm_data_bersih.csv), [`riwayat_pelatihan_cnn.csv`](csv/riwayat_pelatihan_cnn.csv), and [`riwayat_varian_cnn.csv`](csv/riwayat_varian_cnn.csv). The expanded CNN result and training-history tables are also provided as Supplementary Tables S2 and S3.

## Statistical corrections

- `ablasi_cv_perbandingan.csv` retains the Nadeau–Bengio corrected paired-test p-values and adds `p_holm_11_kontras_auc` for the family of 11 AUC contrasts with `site_id`.
- `fairness_cv_oof_selisih.csv` retains raw within-site permutation p-values and adds Bonferroni-adjusted columns for the 12 tests (six groupings/features × two metrics).

The corresponding notebook code generates these correction columns when rerun.

## Figures

All six final manuscript JPEG figures are committed under [`figures/manuscript/`](figures/manuscript/):

| Manuscript figure | File |
|---|---|
| Figure 1 | [`Figure_1.jpg`](figures/manuscript/Figure_1.jpg) |
| Figure 2 | [`Figure_2.jpg`](figures/manuscript/Figure_2.jpg) |
| Figure 3 | [`Figure_3.jpg`](figures/manuscript/Figure_3.jpg) |
| Figure 4 | [`Figure_4.jpg`](figures/manuscript/Figure_4.jpg) |
| Figure 5 | [`Figure_5.jpg`](figures/manuscript/Figure_5.jpg) |
| Figure 6 | [`Figure_6.jpg`](figures/manuscript/Figure_6.jpg) |

The [figure README](figures/README.md) provides the figure captions and folder mapping. The other figure directories contain computational outputs: [confusion matrices](figures/confusion_matrix/) and [CNN training curves](figures/training-curves/). Those notebook-level outputs are retained separately from the six final manuscript figures.
