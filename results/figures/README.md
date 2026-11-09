# Figure inventory and manuscript mapping

The six final JPEG figures supplied in `Figures_JET.zip` were visually checked against the captions in the 9 November 2026 manuscript draft. They are publication-ready source assets at 300 DPI. They have **not yet been committed to this repository**, so the paths below are the intended repository names rather than existing files.

| Manuscript figure | Caption / content | Intended repository path |
|---|---|---|
| Figure 1 | Overall experimental pipeline | `manuscript/figure_1.jpg` |
| Figure 2 | Test accuracy of five algorithms under three protocols on clean Palm data | `manuscript/figure_2.jpg` |
| Figure 3 | Paired AUC difference relative to Original for pooled LightGBM with site_id (repeated 5×5 CV) | `manuscript/figure_3.jpg` |
| Figure 4 | AUC of pooled and Palm-only models under image degradations (80:20 split) | `manuscript/figure_4.jpg` |
| Figure 5 | Confusion matrices of reference AlexNet, MobileNetV2 with early stopping, and pooled Otsu | `manuscript/figure_5.jpg` |
| Figure 6 | Training histories under 70:10:20 for AlexNet-A, AlexNet-B, and MobileNetV2 with early stopping | `manuscript/figure_6.jpg` |

The existing `confusion_matrix/` and `training-curves/` folders contain notebook-level outputs. They are retained as computational artifacts and are not substitutes for the six final manuscript figures listed above.

When adding the final assets, preserve the original figure content and use the intended filenames. The image files should be committed without changing their plotted values or captions.
