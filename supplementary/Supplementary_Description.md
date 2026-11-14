# Supplementary material description

## Supplementary Table S1 — Full baseline results on clean Palm data

S1 reports the clean-Palm baseline metrics under 70:10:20 and 80:10:10 splits. The two SVM parameter configurations are retained separately. Metrics include confusion counts, accuracy, precision, sensitivity, specificity, F1-score, test AUC, validation accuracy/AUC, support counts, and the majority-class baseline.

The classical model rows are sourced from `baseline_palm_data_bersih.csv`; reference AlexNet rows from `baseline_cnn_palm_data_bersih.csv`; and MobileNetV2 early-stopping rows from `varian_cnn_palm_data_bersih.csv`.

## Supplementary Table S2 — CNN configurations

S2 combines four reference CNN runs and six author-modified/early-stopping runs. It contains model configuration, confusion counts, test and validation metrics, predicted-anemic percentage, and stopping/best epochs where recorded.

## Supplementary Table S3 — CNN training history

S3 contains the epoch-wise reference and variant training history, including split, model, epoch, training/validation accuracy, and training/validation loss. It is bundled inside the consolidated results ZIP.

## Reproducibility

The supplementary files are sourced from the latest experiment CSVs. The experiment notebooks document data preparation, split schemes, augmentation, model settings, and evaluation procedures.
