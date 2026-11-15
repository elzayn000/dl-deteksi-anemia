# Experiment notebooks

This directory contains the saved Jupyter notebooks used to audit the dataset and run experiments for the anemia-detection study. They are numbered 16–25 to preserve the research workflow and are designed primarily for Google Colab.

## Notebook index

| Notebook | Purpose | Main outputs / connection |
|---|---|---|
| `16_Dataset_Cleaning_v3.ipynb` | Backs up the Drive dataset, audits label typos, applies corrected filename renaming, and performs the documented cleaning checks. | Cleaning statistics, typo audit, and rename-list artifacts; see `../results/audit/` and `../results/csv/large/`. |
| `17_Pooling_Konsisten.ipynb` | Compares single-site and pooled experiments across Palm, Nail, and Conjunctiva, including feature and split variants. | `hasil_eksperimen_konsisten.csv`; manuscript pooling results. |
| `18_Robustness_Konsisten.ipynb` | Evaluates robustness to Gaussian noise, low light, Gaussian blur, and image rotation. | `hasil_robustness_konsisten.csv`; robustness table export. |
| `19_Replikasi_Protokol_Paper.ipynb` | Compares augmentation-before-splitting, split-before-augmentation, and no-augmentation protocols on Palm data. | `replikasi_protokol_paper.csv`; protocol-replication table. |
| `20_Baseline_Palm_Data_Bersih.ipynb` | Re-evaluates classical machine-learning baselines on cleaned Palm data using the reported split schemes. | `baseline_palm_data_bersih.csv`; detailed baseline export in Supplementary Table S1. |
| `21_Baseline_CNN_Palm_Data_Bersih.ipynb` | Trains the reference AlexNet and MobileNetV2 baselines on cleaned Palm data. | `baseline_cnn_palm_data_bersih.csv`, `riwayat_pelatihan_cnn.csv`, and the CNN training curve; see S2–S3. |
| `22_Varian_CNN_Modifikasi_Penulis.ipynb` | Evaluates author-modified CNN configurations, including regularization/optimizer variants and early stopping. | `varian_cnn_palm_data_bersih.csv`, `riwayat_varian_cnn.csv`, and the variant training curve; see S2–S3. |
| `23_Ablasi_Segmentasi_Normalisasi.ipynb` | Tests ROI segmentation and color-normalization treatments, with single-split and repeated cross-validation analyses. | Ablation summaries/comparisons and the feature-level `fitur_ablasi.csv` intermediate. |
| `24_Fairness_Kecerahan_Citra.ipynb` | Examines performance across image-brightness groupings and evaluates paired contrasts. | The `fairness_*.csv` outputs; brightness-group and contrast tables. |
| `25_Kontras_Ablasi_Tambahan.ipynb` | Calculates additional paired ablation contrasts and sensitivity analyses for empty masks. | `ablasi_kontras_tambahan.csv` and `ablasi_mask_kosong.csv`; sensitivity table export. |

## Recommended execution order

1. **Prepare the dataset.** Download the source records listed in `../dataset-info/DATASET_GUIDE.md` and arrange them as `Dataset_Multisite/Palm/`, `Dataset_Multisite/Nail/`, and `Dataset_Multisite/Conjunctiva/`.
2. **Run Notebook 16 as a sequential workflow, not as a read-only audit.** It creates a timestamped backup, audits the typo list, runs an initial cleaning attempt, restores the backup, then runs the corrected `FIXED v2` cleaning step and final verification. Keep the cells in order: do not stop after the first cleaning attempt or skip the restore step. Check that the backup contains Palm, Nail, and Conjunctiva before allowing the final cleaning step to modify the Drive dataset. The final authoritative cleaning summary is `results/audit/laporan_pembersihan_drive.json`.
3. **Run the analysis notebooks.** Notebooks 17–24 cover pooling, robustness, protocol replication, baselines, CNNs, ablation, and brightness-group fairness.
4. **Run Notebook 25 after Notebook 23.** Notebook 25 reads the feature-level ablation data produced by Notebook 23; it does not reconstruct those features from the images.

## Environment and paths

- The notebooks are intended for Google Colab and Google Drive.
- The common dataset path is `/content/drive/MyDrive/Dataset_Multisite`.
- Output folders used by saved notebook versions include `hasil_revisi` and `hasil_revisi_v2`. Check the `BASE` and `OUT` variables in each notebook before execution.
- Notebook 21 recommends a Colab GPU runtime for CNN training. Check each notebook's own runtime notes rather than assuming every notebook needs a GPU.
- The root `requirements.txt` records packages/versions observed in the notebooks. Colab's runtime may differ, so resolve compatible versions if an installation conflict occurs.

## Important input dependency for Notebook 25

The feature-level intermediate is stored in this repository as `../results/csv/large/fitur_ablasi.csv.gz`. Pandas can read the compressed file directly with `pd.read_csv("fitur_ablasi.csv.gz")`. If Notebook 25 expects an uncompressed `fitur_ablasi.csv` in the Drive output folder, either decompress/copy this file under that name or rerun Notebook 23 to regenerate it.

## Reproducibility notes

Several experiment notebooks set a random seed (commonly 42) and sort file names before processing. For reproducibility, keep the same dataset version, file ordering, split configuration, and library versions. Do not silently rename or add source images after the cleaning/leakage audit.

Raw source images are not included in this repository. Follow the original dataset terms and do not upload identifiable or restricted pediatric data.
