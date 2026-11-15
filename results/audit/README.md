# Dataset audit records

This directory contains JSON summaries recorded during dataset filename correction and cleaning. They document processing operations and intermediate counts; they are not model-evaluation result files.

| File | Recorded information |
|---|---|
| `stats_pembersihan.json` | Summary counts for successful renames, duplicate removal, numbered-copy removal, and timestamped execution |
| `stats_pembersihan_v2.json` | A later cleaning-statistics snapshot with updated numbered-copy and variant-removal counts |
| `laporan_pembersihan_drive.json` | Expanded audit report, including operation counts, intermediate site distribution, verification checks, and backup-folder location |

## Interpreting the counts

The expanded report records an intermediate post-cleaning set of 1,567 images (904 anemic and 663 non-anemic): Palm 520, Nail 532, and Conjunctiva 515. The final experiment set is smaller: 1,563 images (901 anemic and 662 non-anemic), because four Nail images were excluded during the later leakage audit. Use the final experiment counts for manuscript results; retain these JSON files as historical audit records.

## Handling

These files are retained as audit evidence. Do not overwrite historical counts to make them equal to the final experiment set. If a new cleaning pass is performed, save a new, clearly dated audit output and document which dataset version it describes.
