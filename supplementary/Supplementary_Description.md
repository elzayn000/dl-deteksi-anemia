# Supplementary material description

## Supplementary Table S1 — Full baseline results on clean Palm data

S1 reports full model-level metrics for the clean Palm baseline under the 70:10:20 and 80:10:10 train/validation/test schemes. It contains 14 algorithm families; the two SVM parameter configurations are retained as separate rows, giving 15 configuration rows per split and 30 result rows in total. Metrics include TP, TN, FP, FN, accuracy, precision, sensitivity, specificity, F1-score, test AUC, validation accuracy/AUC, support counts, and majority-class baseline.

Classical-model rows are sourced from `baseline_palm_data_bersih.csv`; reference AlexNet rows from `baseline_cnn_palm_data_bersih.csv`; and MobileNetV2 early-stopping rows from `varian_cnn_palm_data_bersih.csv`.

## Supplementary Table S2 — CNN configurations

S2 combines four reference CNN runs and six author-modified/early-stopping runs. It includes model configuration, confusion counts, test and validation metrics, predicted-anemic percentage, and stopping/best epochs where recorded.

## Supplementary Table S3 — CNN training history

S3 contains epoch-wise training and validation accuracy/loss for the reference and author-modified CNN runs. The latest 171-row CSV is included in the source CSV archive.

## Reproducibility and interpretation

The CSV tables are sourced from the latest experiment outputs. The notebooks document data preparation, split schemes, augmentation, model configurations, and evaluation procedures. Brightness groups are image-derived proxies, not validated or self-reported skin-tone measurements; subject-level separation could not be verified because subject identifiers were unavailable.
