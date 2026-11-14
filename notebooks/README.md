# Experiment notebooks

The notebook source files 16–25 are not included in this repository revision. This index documents the role of each notebook and its principal output; the associated result CSVs and manuscript-facing tables are committed under [../results/csv/](../results/csv/).

| Notebook | Purpose | Main output |
|---|---|---|
| `16_Dataset_Cleaning_v3.ipynb` | Correct Nail filename typos, audit duplicates/variants, and prepare the final leakage-checked set. | Cleaning audit and final dataset statistics |
| `17_Pooling_Konsisten (2).ipynb` | Compare Palm, Nail, Conjunctiva, and pooled models under consistent splits. | `hasil_eksperimen_konsisten.csv` |
| `18_Robustness_Konsisten (1).ipynb` | Test Gaussian noise, low illumination, blur, and rotation. | `hasil_robustness_konsisten.csv` and confusion matrices |
| `19_Replikasi_Protokol_Paper (2).ipynb` | Compare augment-then-split, split-then-augment, and no-augmentation protocols. | `replikasi_protokol_paper.csv` |
| `20_Baseline_Palm_Data_Bersih (1).ipynb` | Train classical ML baselines on clean Palm images. | `baseline_palm_data_bersih.csv` |
| `21_Baseline_CNN_Palm_Data_Bersih.ipynb` | Train reference AlexNet and MobileNetV2 baselines. | CNN baseline and reference training-history CSVs |
| `22_Varian_CNN_Modifikasi_Penulis.ipynb` | Evaluate author-modified AlexNet variants and MobileNetV2 with early stopping. | CNN variant metrics and training history |
| `23_Ablasi_Segmentasi_Normalisasi.ipynb` | Evaluate ROI segmentation and color-normalization treatments. | Ablation summaries, paired contrasts, and feature-level output |
| `24_Fairness_Kecerahan_Citra (1).ipynb` | Analyze out-of-fold metrics across ITA and within-site L* brightness groups. | Fairness subgroup and paired-contrast CSVs |
| `25_Kontras_Ablasi_Tambahan.ipynb` | Calculate additional paired ablation contrasts and empty-mask sensitivity. | Additional ablation contrasts and mask-count CSVs |

## Execution notes

- Expected Google Drive input: `/content/drive/MyDrive/Dataset_Multisite`.
- Output path used by many notebook cells: `/content/drive/MyDrive/hasil_revisi_v2`. Update paths if needed.
- Notebook 21 and 22 use TensorFlow/Keras; a Colab GPU is recommended.
- Notebook 25 depends on feature-level output from Notebook 23.
