# Supplementary material

This folder contains the reader-facing supplementary tables associated with the manuscript **“Robust Anemia Detection from Pallor Images Considering Skin Pigmentation and Illumination Variability.”**

## Files

| File | Contents |
|---|---|
| [Supplementary Table S1](Supplementary_Table_S1_Full_Baseline.csv) | Full Palm baseline metrics for 14 algorithm families, with the two SVM configurations shown separately, under 70:10:20 and 80:10:10 splits. |
| [Supplementary Table S2](Supplementary_Table_S2_CNN_Experiments.csv) | Full CNN baseline and author-modified variant metrics, including the 10-epoch MobileNetV2 result and early-stopping results. |
| [Supplementary Table S3](Supplementary_Table_S3_CNN_Training_History.csv) | Epoch-wise training and validation accuracy/loss for the CNN runs. |
| [Supplementary description](Supplementary_Description.md) | Definitions, source-file mapping, and notes for interpreting the tables. |

## Use in the manuscript

Supplementary Table S1 provides expanded per-configuration baseline results (including precision, sensitivity, specificity, F1-score, and validation AUC where those values are available from the saved runs or manuscript). The Stacking Ensemble metrics are synchronized to the manuscript; fields not reported in the manuscript are left blank rather than copied from the earlier run. Tables S2 and S3 provide the additional CNN configuration and training-history detail discussed alongside the CNN results.

The tables are CSV files to keep them easy to inspect, version, and reuse. They can be opened in Excel or imported into spreadsheet software. The committed source CSVs remain available under `../results/csv/`.

## Important counting note

The manuscript describes 14 algorithm families. SVM has two reported parameter configurations, so Table S1 has 15 configuration rows per split (30 result rows across the two splits). The two SVM settings must not be collapsed into one metric row.
