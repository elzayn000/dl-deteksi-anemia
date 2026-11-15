# Result figures

This directory contains individual vector figures exported from the experiment notebooks. SVG is used so plots remain sharp when zoomed or placed in a manuscript.

## Confusion matrices

Location: `confusion_matrix/`

| File | Notebook association |
|---|---|
| `cm_nb17_80_20.svg` | Notebook 17 — pooling experiment, 80:20 scheme |
| `cm_nb18_pooled_80_20.svg` | Notebook 18 — pooled robustness experiment, 80:20 scheme |
| `cm_nb19.svg` | Notebook 19 — protocol replication |
| `cm_nb20_70_10_20.svg` | Notebook 20 — baseline experiment, 70:10:20 scheme |
| `cm_nb21.svg` | Notebook 21 — CNN baseline |
| `cm_nb23.svg` | Notebook 23 — segmentation/normalization ablation |
| `cm_nb24.svg` | Notebook 24 — brightness-group analysis |

## CNN training curves

Location: `training-curves/`

| File | Description |
|---|---|
| `kurva_pelatihan_cnn.svg` | Training history for the reference CNN experiments |
| `kurva_varian_cnn.svg` | Training history for the author-modified CNN variants |

## Manuscript figures

Location: `manuscript/`

The six JPEG files `Figure_1.jpg` through `Figure_6.jpg` are legacy assets retained from the previous repository version. They are **not** the nine figure images embedded in the latest `Draft_v2_0_21_Fig1_Demo` manuscript. The SVG files above are experiment diagnostic outputs (confusion matrices and CNN training curves); the latest paper's composite Figures 1–9 remain embedded in the manuscript document rather than exported individually in this directory. Do not treat the six legacy JPEGs as the current paper's figure set.
