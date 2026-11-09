# Experiment notebooks

Run the notebooks in Google Colab after arranging the source datasets as described in [../dataset-info/DATASET_GUIDE.md](../dataset-info/DATASET_GUIDE.md).

| Notebook | Purpose | Principal output |
|---|---|---|
| `16_Audit_Dataset (2).ipynb` | Audit filenames, MD5 duplicates, conflicting labels, and file variants. | `audit_kategori_file.csv`, `file_terpakai_md5.csv` |
| `17_Pooling_Konsisten (2).ipynb` | Compare Palm, Nail, Conjunctiva, and pooled models, with and without cleaning. | `hasil_eksperimen_konsisten.csv` |
| `18_Robustness_Konsisten (1).ipynb` | Test Gaussian noise, low illumination, blur, and rotation. | `hasil_robustness_konsisten.csv` |
| `19_Replikasi_Protokol_Paper (2).ipynb` | Compare augment-then-split, split-then-augment, and no-augmentation protocols. | `replikasi_protokol_paper.csv` |
| `20_Baseline_Palm_Data_Bersih (1).ipynb` | Train classical ML baselines on clean Palm images. | `baseline_palm_data_bersih.csv` |
| `21_Baseline_CNN_Palm_Data_Bersih.ipynb` | Train the reference AlexNet configuration and 10-epoch MobileNetV2 baseline. | `baseline_cnn_palm_data_bersih.csv`, training history and curve |
| `22_Varian_CNN_Modifikasi_Penulis.ipynb` | Evaluate author-modified AlexNet variants and MobileNetV2 with early stopping. | `varian_cnn_palm_data_bersih.csv`, variant history and curve |
| `23_Ablasi_Segmentasi_Normalisasi.ipynb` | Evaluate ROI segmentation and color-normalization treatments. | Ablation CSV files and `fitur_ablasi.csv` |
| `24_Fairness_Kecerahan_Citra (1).ipynb` | Analyze out-of-fold performance across image-brightness groups. | Fairness CSV files |
| `25_Kontras_Ablasi_Tambahan.ipynb` | Calculate additional paired ablation contrasts and empty-mask sensitivity. | `ablasi_kontras_tambahan.csv`, `ablasi_mask_kosong.csv` |

## Execution notes

- The notebooks use seed 42 and sorted filename order.
- The expected Google Drive paths are `/content/drive/MyDrive/Dataset_Multisite` for the data and `/content/drive/MyDrive/hasil_revisi` for outputs. Update the configuration cell if your paths differ.
- Notebooks 20, 17, 18, 23, 24, and 25 primarily use classical ML / image-processing dependencies. Notebook 21 and 22 use TensorFlow/Keras; a Colab GPU is recommended for training.
- Notebook 25 depends on `fitur_ablasi.csv` produced by notebook 23.
- The notebooks contain the detailed methods and parameter settings; this index is only a navigation aid.
