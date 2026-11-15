# Dataset audit records

This directory contains JSON summaries from the dataset filename audit and cleaning workflow. They document cleaning operations and the transition from the cleaned Drive dataset to the final experiment set.

| File | Recorded information | Status |
|---|---|---|
| `stats_pembersihan.json` | Rename, MD5-duplicate, and numbered-copy counts from the initial logged cleaning pass (2026-11-11 08:02:21) | Historical operation log; its MD5 and numbered-copy totals agree with the final audit |
| `stats_pembersihan_v2.json` | Snapshot from an intermediate execution (2026-11-11 08:12:59), reporting 4,604 numbered-copy deletions and 5 variant deletions | **Intermediate only; do not use as the final cleaning summary** |
| `laporan_pembersihan_drive.json` | Expanded final Drive cleaning report (2026-11-11 08:20:58), including operation counts, distribution, verification checks, and backup path | **Authoritative Drive-cleaning summary** |

## Final counts to use

The authoritative `laporan_pembersihan_drive.json` records the cleaned Drive dataset as 1,567 images: Palm 520 (302 anemic, 218 non-anemic), Nail 532 (310, 222), and Conjunctiva 515 (292, 223), for 904 anemic and 663 non-anemic images in total. It records 1,625 typo-prefix renames, 6,617 MD5 duplicate deletions, 5,488 numbered-copy deletions, and no remaining typo, MD5 duplicate, numbered-copy, or variant files. The audit also records one conflicting-label pair.

The final experiments use **1,563 images (901 anemic, 662 non-anemic)**. Four Nail images were excluded later by the partition-integrity check because variants crossed data partitions. This is the denominator used in the final report and manuscript tables.

## Interpreting the intermediate snapshot

`stats_pembersihan_v2.json` is retained to preserve the audit trail, not to define the final dataset. Its 4,604 numbered-copy and 5 variant-deletion counts belong to an intermediate cleaning pass. They are superseded by the later expanded report in `laporan_pembersihan_drive.json` and should not be cited as the final cleaning totals.

Do not overwrite historical audit files to make all snapshots identical. If another cleaning pass is performed, save a new dated report and state which dataset version it describes.
