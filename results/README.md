# Experiment results

This directory contains the exported experiment outputs used to inspect and support the manuscript results. The files are organized by data type rather than by notebook execution order.

## Directory map

| Path | Contents |
|---|---|
| `csv/` | Source experiment outputs and manuscript-aligned Tables I–XI |
| `csv/large/` | Compressed detailed CSV artifacts, including the feature-level ablation data |
| `audit/` | JSON summaries from dataset cleaning and file-audit steps |
| `figures/confusion_matrix/` | Seven confusion-matrix figures in SVG |
| `figures/training-curves/` | Two CNN training curves in SVG |

## Where to start

- For values intended to map directly to manuscript tables, use the `table_*.csv` exports in [`csv/README.md`](csv/README.md).
- For experiment-level detail, use the baseline, pooling, robustness, ablation, fairness, and CNN-history CSVs described in that same guide.
- For the documented cleaning history, read [`audit/README.md`](audit/README.md).
- For plot filenames and their associated experiments, read [`figures/README.md`](figures/README.md).

## Dataset-count interpretation

The final reported experiment set contains 1,563 images (901 anemic, 662 non-anemic). The cleaning audit JSON records an earlier intermediate set of 1,567 images (904 anemic, 663 non-anemic), before four Nail images were excluded during the final leakage audit. These counts describe different processing stages and should not be treated as conflicting final totals.

## Data integrity

Do not edit exported CSV values manually to make them match a draft table. If an output needs to change, regenerate it from the corresponding notebook and document the change. Preserve the distinction between source experiment outputs, manuscript-facing table exports, and supplementary tables.
