# Supplementary material description

## Supplementary Table S1 — Full baseline results on clean Palm data

Table S1 reports the full model-level metrics for the 519 clean Palm images under the 70:10:20 and 80:10:10 train/validation/test schemes. It contains 14 algorithm families: Naive Bayes, k-nearest neighbors, support vector machine, decision tree, random forest, logistic regression, XGBoost, artificial neural network (MLP), AdaBoost, LightGBM, CatBoost, stacking ensemble, AlexNet, and MobileNetV2. The two SVM parameter settings are retained as separate configurations.

The reported metrics are accuracy, precision, sensitivity, specificity, F1-score, test AUC, validation accuracy, and validation AUC. TP, TN, FP, and FN are included to make the test counts transparent. Values ending in `_pct` are percentages. `n_train_augmented_rows` is the number of training rows after the five-view augmentation used by the relevant Palm baseline; it is not the number of distinct source photographs.

The selected AlexNet row uses the reference configuration in the baseline CNN results. The MobileNetV2 row uses the early-stopping configuration reported in the manuscript (maximum 40 epochs). Its separate 10-epoch baseline result is retained in Table S2 for completeness. For Stacking Ensemble, Table S1 takes accuracy, precision, sensitivity, specificity, F1, test AUC, and validation AUC from Appendix A1 of the final experiment report. TP/TN/FP/FN are reconstructed from the reported test supports and rounded sensitivity/specificity; validation accuracy remains blank because Appendix A1 does not report it.

## Supplementary Table S2 — CNN configurations

Table S2 lists all CNN configurations present in the committed CNN result CSVs: the reference AlexNet and 10-epoch MobileNetV2 baselines, plus AlexNet-A, AlexNet-B, and MobileNetV2 with early stopping. Author-modified variants are labelled as such and are not substituted for the reference AlexNet baseline. The table includes confusion counts, test and validation metrics, predicted-anemic percentage, and the stopped/best epoch where recorded.

## Supplementary Table S3 — CNN training history

Table S3 contains epoch-wise training accuracy, loss, validation accuracy, and validation loss from the two committed CNN training-history files. These are the recorded learning histories; they are not new experiments.

## Source data and reproducibility

All three tables were assembled from the CSVs committed in `results/csv/`:

- `baseline_palm_data_bersih.csv`
- `baseline_cnn_palm_data_bersih.csv`
- `varian_cnn_palm_data_bersih.csv`
- `riwayat_pelatihan_cnn.csv`
- `riwayat_varian_cnn.csv`

Most metrics are organized from the committed experimental result CSVs. The Stacking Ensemble row in S1 is synchronized to Appendix A1 of the uploaded final experiment report. The manuscript's Table II remains unchanged: it reports selected baselines with accuracy and test AUC for both split schemes. The earlier computational snapshot is preserved separately as baseline_palm_data_bersih_computational_run.csv. See the notebooks for the exact feature extraction, split, augmentation, and model settings.
