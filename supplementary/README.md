# Supplementary tables

This directory contains three CSV exports intended to accompany the manuscript. S1 and S2 contain model-level evaluation details; S3 preserves epoch-by-epoch CNN training history.

| File | Contents | Main fields |
|---|---|---|
| `Supplementary_Table_S1_Full_Baseline.csv` | Expanded baseline metrics for the Palm experiments across the 70:10:20 and 80:10:10 split schemes | Algorithm/configuration, split sizes, TP/TN/FP/FN, accuracy, precision, sensitivity, specificity, F1, test/validation AUC, and majority-class baseline |
| `Supplementary_Table_S2_CNN_Experiments.csv` | Reference CNN baselines and author-modified CNN experiments | Model/run type, configuration, split sizes, confusion counts, performance metrics, predicted-anemic percentage, and stopping/best epoch when available |
| `Supplementary_Table_S3_CNN_Training_History.csv` | Epoch-level training and validation history for CNN runs | Split scheme, algorithm, epoch, accuracy/loss, validation accuracy/loss, run series, and source CSV |

## Relationship to the main results

- S1 expands the baseline results summarized in `../results/csv/table_ii_selected_baselines.csv` and the corresponding baseline CSV exports.
- S2 provides additional detail for the CNN rows and configurations reported in the baseline/variant outputs.
- S3 contains the per-epoch histories associated with `riwayat_pelatihan_cnn.csv` and the variant training history.

## Data format

All three files are UTF-8 CSV files with a header row. S3 is stored as an ordinary `.csv` file in this branch (not `.csv.gz`). Use a CSV-aware reader and preserve decimal values, percentage units, and empty fields as recorded.

These files contain exported research results, not source pediatric images. For dataset origins, local folder layout, and sample counts, see `../dataset-info/DATASET_GUIDE.md` from the repository root.
