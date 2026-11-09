# Robust Anemia Detection from Pallor Images

Research code and experimental results for the manuscript:

**Robust Anemia Detection from Pallor Images Considering Skin Pigmentation and Illumination Variability**

This repository contains the analysis notebooks, tabular outputs, figures, and supplementary result tables associated with the study.

## Study overview

The study re-evaluates image-based anemia screening under a leakage-aware protocol using three pediatric pallor-image datasets (palm, fingernail, and conjunctiva). The audited and cleaned collection contains 1,345 images: 519 Palm, 312 Nail, and 514 Conjunctiva images.

The experiments cover 14 algorithm families on clean Palm data (with two SVM configurations), replication of an augmentation-before-splitting protocol, single-site versus pooled models, ROI segmentation and color-normalization ablations, image-brightness subgroup analysis, and robustness to image degradations.

## Repository structure

```text
.
├── README.md
├── CITATION.cff
├── requirements.txt
├── .gitignore
├── dataset-info/
│   └── DATASET_GUIDE.md
├── notebooks/
│   ├── README.md
│   └── 16–25 experiment notebooks
├── results/
│   ├── README.md
│   ├── csv/
│   └── figures/
│       ├── confusion_matrix/
│       └── training-curves/
└── supplementary/
    ├── README.md
    ├── Supplementary_Table_S1_Full_Baseline.csv
    ├── Supplementary_Table_S2_CNN_Experiments.csv
    ├── Supplementary_Table_S3_CNN_Training_History.csv
    └── Supplementary_Description.md
```

The notebook filenames retain the original upload suffixes (for example, `(1)` or `(2)`) where present. See [notebooks/README.md](notebooks/README.md) for the exact filenames and their purpose.

## Dataset access

The source images are not redistributed in this repository. Obtain them from the original Mendeley Data records and follow their terms of use:

- Palm: [10.17632/ccr8cm22vz.1](https://doi.org/10.17632/ccr8cm22vz.1)
- Nail: [10.17632/2xx4j3kjg2.1](https://doi.org/10.17632/2xx4j3kjg2.1)
- Conjunctiva: [10.17632/nt7r8hv2pz.1](https://doi.org/10.17632/nt7r8hv2pz.1)

After obtaining the data, arrange the folders as described in [dataset-info/DATASET_GUIDE.md](dataset-info/DATASET_GUIDE.md). Do not commit raw images, subject identifiers, or other restricted data to this repository.

## Quick start (Google Colab)

1. Obtain the three datasets from their source records.
2. Upload or mount a Google Drive folder named `Dataset_Multisite` with the subfolders `Palm/`, `Nail/`, and `Conjunctiva/`.
3. Open the required notebook from `notebooks/` in Google Colab.
4. Check the configuration cell for the dataset path and output path. The notebooks currently use `/content/drive/MyDrive/Dataset_Multisite` and write generated CSV files to `/content/drive/MyDrive/hasil_revisi`.
5. Run the notebook cells in order. The classical ML notebooks install XGBoost, LightGBM, and CatBoost as needed. The CNN notebooks use TensorFlow/Keras; a Colab GPU runtime is recommended for CNN training.
6. Compare generated outputs with the committed files in `results/csv/`.

The experiments use seed 42 and sorted filename order. Some analyses use repeated stratified 5-fold cross-validation with 5 repeats. Each notebook documents its inputs, outputs, and experimental role.

## Notebook map

See [notebooks/README.md](notebooks/README.md) for the exact notebook-to-experiment mapping.

## Results and supplementary material

- [All committed CSV outputs](results/csv/)
- [Confusion matrices](results/figures/confusion_matrix/)
- [CNN training curves](results/figures/training-curves/)
- [Supplementary material index](supplementary/README.md)
- [Supplementary Table S1 — full Palm baseline metrics](supplementary/Supplementary_Table_S1_Full_Baseline.csv)
- [Supplementary Table S2 — CNN configurations and results](supplementary/Supplementary_Table_S2_CNN_Experiments.csv)
- [Supplementary Table S3 — CNN epoch-wise training history](supplementary/Supplementary_Table_S3_CNN_Training_History.csv)

Table S1 provides the full per-configuration baseline metrics requested in the manuscript. It contains 14 algorithm families; SVM is represented by two separately reported configurations. The CSV therefore has 15 configuration rows for each of the two train/validation/test split schemes.

## Computational environment

The saved notebook outputs report Python 3.13.16 or 3.13.18, NumPy 2.4.6, pandas 2.2.3, OpenCV 4.14.0, scikit-learn 1.6.1, and LightGBM 4.6.0. The Python patch version differs between recorded notebook sessions. Versions for some optional packages (including TensorFlow, XGBoost, and CatBoost) were not consistently recorded; see the notebook installation and output cells. The accompanying `requirements.txt` records the known versions and lists the remaining dependencies without claiming unverified pins.

## Interpretation and limitations

The image-brightness groups are proxies derived from image pixels, not validated or self-reported skin-tone measurements. Subject identifiers were unavailable, so subject-level separation could not be verified. The manuscript discusses these and other limitations; the reported results should be interpreted in that context.

## Citation

If you use the code or supplementary tables, cite the associated manuscript and this repository. A machine-readable repository citation is provided in [CITATION.cff](CITATION.cff). The manuscript is not assigned a DOI in this repository yet.

## Software license

No separate software license has been added. Please contact the authors before redistributing or reusing the code beyond the permissions that apply to the source datasets. A license should be added only after the code contributors have agreed on its terms.
