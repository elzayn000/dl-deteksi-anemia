# Robust Anemia Detection from Pallor Images

Research code, experiment outputs, supporting figures, and supplementary material for **Robust Anemia Detection from Pallor Images Considering Skin Pigmentation and Illumination Variability**.

## Final experiment set

The final reported experiment set contains **1,563 images (901 anemic, 662 non-anemic)**: Palm 520 (302/218), Nail 528 (307/221), and Conjunctiva 515 (292/223). The cleaned collection contained 1,567 images before four Nail images were excluded during the final leakage audit.

## Repository map

- `dataset-info/DATASET_GUIDE.md`: source dataset records, local folder layout, and final sample counts.
- `notebooks/README.md`: experiment notebook index and execution instructions.
- `results/csv/`: refreshed source result CSVs and manuscript-aligned Tables I–XI.
- `results/releases/supporting_figures_svg_2026-11-14.tar.xz`: seven confusion matrices and two CNN training curves in SVG format.
- `results/figures/manuscript/`: six final manuscript JPEG figures.
- `supplementary/`: Supplementary Tables S1–S2 and compressed S3 training history.

## Dataset access

Source images are not redistributed in this repository. Obtain them from the original Mendeley Data records and follow their terms:
- Palm: [10.17632/ccr8cm22vz.1](https://doi.org/10.17632/ccr8cm22vz.1)
- Nail: [10.17632/2xx4j3kjg2.1](https://doi.org/10.17632/2xx4j3kjg2.1)
- Conjunctiva: [10.17632/nt7r8hv2pz.1](https://doi.org/10.17632/nt7r8hv2pz.1)

Arrange images as described in [DATASET_GUIDE.md](dataset-info/DATASET_GUIDE.md). Do not commit raw pediatric images, subject identifiers, or restricted data.

## Reproduction

The experiment notebooks are intended for Google Colab. Expected input path: `/content/drive/MyDrive/Dataset_Multisite`; many outputs use `/content/drive/MyDrive/hasil_revisi_v2`. Update path settings if needed. See [notebooks/README.md](notebooks/README.md).

## Results and supplementary files

The manuscript-facing CSV exports for Tables I–XI are available individually in [results/csv/](results/csv/). Detailed current result files include the clean-Palm baselines, CNN baseline, ablation, and fairness CSVs. The supporting figure archive is [available here](results/releases/supporting_figures_svg_2026-11-14.tar.xz); extract it inside `results/figures/`.

- [Supplementary Table S1 — full Palm baseline metrics](supplementary/Supplementary_Table_S1_Full_Baseline.csv)
- [Supplementary Table S2 — CNN experiments](supplementary/Supplementary_Table_S2_CNN_Experiments.csv)
- [Supplementary Table S3 — CNN epoch history (CSV.GZ)](supplementary/Supplementary_Table_S3_CNN_Training_History.csv.gz)

The current PR does not add the notebook source files 16–25 themselves; `notebooks/README.md` describes their functions and required outputs. The separately prepared notebook archive is available in the conversation attachment.

## Interpretation and limitations

Brightness groups are image-derived proxies, not validated or self-reported skin-tone measurements. Subject identifiers were unavailable, so subject-level separation could not be verified. Interpret results with these limitations in mind.

## Citation

If you use the code or supplementary tables, cite the associated research manuscript and this repository. A machine-readable repository citation is provided in [CITATION.cff](CITATION.cff). The manuscript DOI is not recorded in this repository.

## Software license

The original code and documentation contributed by Daniel Halasson Hasibuan, Indra Saputra, and Rasya Halim are released under the [MIT License](LICENSE). The MIT License applies only to the original materials owned by these contributors. Third-party datasets and externally sourced materials remain subject to their respective licenses and terms of use.
