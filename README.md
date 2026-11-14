# Robust Anemia Detection from Pallor Images

Research code, experiment outputs, and supplementary tables for **Robust Anemia Detection from Pallor Images Considering Skin Pigmentation and Illumination Variability**.

## Final experiment set

The final reported experiment set contains **1,563 images (901 anemic, 662 non-anemic)**: Palm 520 (302/218), Nail 528 (307/221), and Conjunctiva 515 (292/223). The cleaned collection contained 1,567 images before four Nail images were excluded during the final leakage audit.

## Repository map

- `dataset-info/DATASET_GUIDE.md`: source dataset records, local folder layout, and final sample counts.
- `notebooks/`: experiment notebooks and run instructions.
- `results/csv/`: source experiment CSVs and manuscript-aligned tables I–XI.
- `results/releases/`: downloadable result-package archive.
- `results/figures/`: manuscript and experiment figures.
- `supplementary/`: standalone key supplementary CSVs and their descriptions.

## Dataset access

Source images are not redistributed in this repository. Obtain them from the original Mendeley Data records and follow their terms:
- Palm: [10.17632/ccr8cm22vz.1](https://doi.org/10.17632/ccr8cm22vz.1)
- Nail: [10.17632/2xx4j3kjg2.1](https://doi.org/10.17632/2xx4j3kjg2.1)
- Conjunctiva: [10.17632/nt7r8hv2pz.1](https://doi.org/10.17632/nt7r8hv2pz.1)

Arrange images as described in [DATASET_GUIDE.md](dataset-info/DATASET_GUIDE.md). Do not commit raw pediatric images, subject identifiers, or restricted data.

## Reproduction

The experiment notebooks are designed for Google Colab. Expected input path: `/content/drive/MyDrive/Dataset_Multisite`; output path: `/content/drive/MyDrive/hasil_revisi_v2`. Update notebook configuration cells if your Drive paths differ. See [notebooks/README.md](notebooks/README.md).

## Results and supplementary files

- [Download the consolidated 14 November 2026 experiment-results ZIP](results/releases/experiment_results_2026-11-14.zip). It contains the current source CSV outputs, Tables I–XI, cleaning JSON summaries, and Supplementary Tables S1–S3.
- [Supplementary Table S1 — full baseline metrics](supplementary/Supplementary_Table_S1_Full_Baseline.csv)
- [Supplementary Table S2 — CNN experiments](supplementary/Supplementary_Table_S2_CNN_Experiments.csv)
- [Results index](results/README.md)

The consolidated ZIP contains the experiment CSVs and table exports. Four large internal CSV artifacts (the full filename audit/rename lists and feature-level ablation file) are not included in this compact release archive. The raw pediatric images are also excluded.

## Interpretation and limitations

Brightness groups are image-derived proxies, not validated or self-reported skin-tone measurements. Subject identifiers were unavailable, so subject-level separation could not be verified. Interpret the results with these limitations in mind.

## Citation and license

Cite the associated manuscript and this repository when using the code or supplementary tables. Third-party datasets and external material remain subject to their own licenses and terms.
