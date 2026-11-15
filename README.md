# Robust Anemia Detection from Pallor Images

Research code, experiment outputs, figures, and supplementary tables for the study **Robust Anemia Detection from Pallor Images Considering Skin Pigmentation and Illumination Variability**.

## Final experiment set

The final reported experiment set contains **1,563 images (901 anemic and 662 non-anemic)** across three image sites:

| Site | Anemic | Non-anemic | Total |
|---|---:|---:|---:|
| Palm | 302 | 218 | 520 |
| Nail | 307 | 221 | 528 |
| Conjunctiva | 292 | 223 | 515 |
| **Pooled** | **901** | **662** | **1,563** |

The dataset-cleaning audit also records an intermediate set of 1,567 images (904 anemic and 663 non-anemic). Four Nail images were subsequently excluded during the final leakage audit; the 1,563-image set is used for the final experiment tables.

## Repository structure

| Path | Contents |
|---|---|
| `dataset-info/` | Dataset source records, expected local folder layout, and sample counts |
| `notebooks/` | Executable experiment notebooks 16–25 and their index |
| `results/audit/` | Dataset-cleaning audit summaries in JSON |
| `results/csv/` | Experiment-level CSV outputs and manuscript-aligned Tables I–XI |
| `results/csv/large/` | Compressed, detailed CSV artifacts that are larger or mainly used for audit/reanalysis |
| `results/figures/confusion_matrix/` | Seven confusion-matrix figures in SVG format |
| `results/figures/training-curves/` | Two CNN training-history figures in SVG format |
| `results/figures/manuscript/` | Six manuscript figure images retained from the previous repository version |
| `supplementary/` | Supplementary Tables S1–S3 in CSV format |

Folder-level guides are provided throughout the repository. Start with [`notebooks/README.md`](notebooks/README.md) for the experiment sequence, [`results/README.md`](results/README.md) for the output map, and [`supplementary/README.md`](supplementary/README.md) for the supplementary tables.

## Dataset access

Raw pediatric images are **not redistributed** in this repository. Obtain the three source datasets from their original Mendeley Data records and follow each record's current license and terms:

- Palm: [10.17632/ccr8cm22vz.1](https://doi.org/10.17632/ccr8cm22vz.1)
- Nail: [10.17632/2xx4j3kjg2.1](https://doi.org/10.17632/2xx4j3kjg2.1)
- Conjunctiva: [10.17632/nt7r8hv2pz.1](https://doi.org/10.17632/nt7r8hv2pz.1)

Arrange the images as described in [`dataset-info/DATASET_GUIDE.md`](dataset-info/DATASET_GUIDE.md): `Dataset_Multisite/{Palm,Nail,Conjunctiva}/`. Do not commit raw pediatric images, subject identifiers, or restricted data.

## Reproducing the experiments

The notebooks were prepared for Google Colab and use Google Drive paths. The default dataset path shown in the notebooks is `/content/drive/MyDrive/Dataset_Multisite`; inspect each notebook's configuration cells and adjust paths when necessary. Package versions recorded by the experiments are listed in [`requirements.txt`](requirements.txt), although Colab's preinstalled environment may require compatible versions.

Recommended order:

1. Review Notebook 16 carefully. It creates a timestamped backup and then performs dataset auditing/cleaning operations. Verify the backup and the resulting dataset before continuing.
2. Run the experiment notebooks 17–24 as needed for the corresponding analysis.
3. Run Notebook 25 after Notebook 23 if the feature-level ablation output is not already available. The repository stores that intermediate artifact as `results/csv/large/fitur_ablasi.csv.gz`; decompress it to the filename expected by Notebook 25 or regenerate it by running Notebook 23.

Notebook 21 is a CNN training workflow. A Colab GPU runtime is recommended to accelerate training, although CPU execution is possible and may take longer. Other notebooks may run on CPU, as noted in their own instructions. See [`notebooks/README.md`](notebooks/README.md) for the purpose, dependencies, and outputs of each notebook.

## Results and supplementary material

- **Manuscript-aligned tables:** Tables I–XI are exported as individual CSV files in [`results/csv/`](results/csv/README.md).
- **Detailed experiment outputs:** Baseline, pooling, robustness, ablation, fairness, and CNN history files are also available in `results/csv/`.
- **Experiment figures:** Seven confusion matrices and two CNN training curves are supplied as individual SVG files. See [`results/figures/README.md`](results/figures/README.md).
- **Manuscript figures:** Six JPEG files are retained separately in `results/figures/manuscript/`.
- **Supplementary tables:** S1 contains the expanded baseline metrics, S2 the CNN experiment results, and S3 the CNN epoch-level training history. See [`supplementary/README.md`](supplementary/README.md).

## Interpretation and limitations

Brightness-based groups are image-derived proxies and must not be interpreted as validated or self-reported skin-pigmentation measurements. Subject identifiers were unavailable, so subject-level separation could not be independently verified. Interpret fairness and generalization results in light of these limitations.

## Citation

If you use the code or supplementary exports, cite the associated research manuscript and this repository. Repository citation metadata is provided in [`CITATION.cff`](CITATION.cff). A manuscript DOI has not been recorded in this repository.

## License

Original code and documentation contributed by Daniel Halasson Hasibuan, Indra Saputra, and Rasya Halim are released under the [MIT License](LICENSE). This license applies only to original materials owned by these contributors. Third-party datasets and externally sourced materials remain subject to their own licenses and terms.
