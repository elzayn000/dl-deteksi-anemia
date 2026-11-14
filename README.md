# Robust Anemia Detection from Pallor Images

Research code, experiment outputs, figures, and supplementary material for **Robust Anemia Detection from Pallor Images Considering Skin Pigmentation and Illumination Variability**.

## Final experiment set

The final reported experiment set contains **1,563 images (901 anemic, 662 non-anemic)**: Palm 520 (302/218), Nail 528 (307/221), and Conjunctiva 515 (292/223). The cleaned collection contained 1,567 images before four Nail images were excluded during the final leakage audit.

## Repository map

- `dataset-info/DATASET_GUIDE.md`: source dataset records, local folder layout, and final sample counts.
- `notebooks/`: notebook index and instructions. The latest notebook source files 16–25 are included in the downloadable archive.
- `results/csv/`: source experiment CSVs and manuscript-aligned tables I–XI.
- `results/audit/`: dataset-cleaning audit JSON files.
- `results/releases/`: dated result, figure, and notebook packages.
- `results/figures/`: six manuscript JPEGs and figure inventory; refreshed supporting SVGs are available in the figures archive.
- `supplementary/`: Supplementary Tables S1–S2 and descriptions.

## Dataset access

Source images are not redistributed in this repository. Obtain them from the original Mendeley Data records and follow their terms:
- Palm: [10.17632/ccr8cm22vz.1](https://doi.org/10.17632/ccr8cm22vz.1)
- Nail: [10.17632/2xx4j3kjg2.1](https://doi.org/10.17632/2xx4j3kjg2.1)
- Conjunctiva: [10.17632/nt7r8hv2pz.1](https://doi.org/10.17632/nt7r8hv2pz.1)

Arrange images as described in [DATASET_GUIDE.md](dataset-info/DATASET_GUIDE.md). Do not commit raw pediatric images, subject identifiers, or restricted data.

## Latest reproducibility packages

- [Source CSVs, manuscript Tables I–XI, cleaning JSON, and Supplementary Tables S1–S3](results/releases/source_csv_tables_2026-11-14.zip)
- [Seven confusion matrices and two CNN training curves (SVG)](results/releases/supporting_figures_svg_2026-11-14.zip). Extract inside `results/figures/`.
- [Experiment notebooks 16–25 (TAR.XZ)](results/releases/notebooks_16_25_2026-11-14.tar.xz). Extract at the repository root.

The CSV archive includes source experiment outputs, manuscript-ready tables, and the current S1–S3 files. Four large internal artifacts (full typo audit, two detailed filename-rename lists, and feature-level ablation data) and raw pediatric images are excluded.

## Manuscript-aligned tables

The table exports are indexed in [results/README.md](results/README.md). Key supplementary files: [Table S1](supplementary/Supplementary_Table_S1_Full_Baseline.csv) and [Table S2](supplementary/Supplementary_Table_S2_CNN_Experiments.csv). The latest Table S3 is included in the source CSV archive.

## Interpretation and limitations

Brightness groups are image-derived proxies, not validated or self-reported skin-tone measurements. Subject identifiers were unavailable, so subject-level separation could not be verified. Interpret the results with these limitations in mind.

## Citation

If you use the code or supplementary tables, cite the associated research manuscript and this repository. A machine-readable repository citation is provided in [CITATION.cff](CITATION.cff). The manuscript DOI is not recorded in this repository.

## Software license

The original code and documentation contributed by Daniel Halasson Hasibuan, Indra Saputra, and Rasya Halim are released under the [MIT License](LICENSE). The MIT License applies only to the original materials owned by these contributors. Third-party datasets and externally sourced materials remain subject to their respective licenses and terms of use.
