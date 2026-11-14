# Dataset guide

## Source records

| Site | Mendeley Data DOI | Local folder |
|---|---|---|
| Palm | [10.17632/ccr8cm22vz.1](https://doi.org/10.17632/ccr8cm22vz.1) | `Dataset_Multisite/Palm/` |
| Nail | [10.17632/2xx4j3kjg2.1](https://doi.org/10.17632/2xx4j3kjg2.1) | `Dataset_Multisite/Nail/` |
| Conjunctiva | [10.17632/nt7r8hv2pz.1](https://doi.org/10.17632/nt7r8hv2pz.1) | `Dataset_Multisite/Conjunctiva/` |

Check the current dataset record and its license statement before reuse or redistribution.

## Expected local layout

```text
Dataset_Multisite/
├── Palm/
├── Nail/
└── Conjunctiva/
```

The notebooks infer labels from `Anemic` and `Non-Anemic` filename prefixes and sort filenames before processing. The Nail audit corrected the misspelled `Anmeic-` prefix while preserving filename suffixes. Do not manually rename files without documenting the change and rerunning the leakage checks.

## Final experimental set

| Site | Anemic | Non-anemic | Total |
|---|---:|---:|---:|
| Palm | 302 | 218 | 520 |
| Nail | 307 | 221 | 528 |
| Conjunctiva | 292 | 223 | 515 |
| **Pooled** | **901** | **662** | **1,563** |

The manuscript also records an intermediate post-cleaning collection of 1,567 images (904 anemic, 663 non-anemic), before four Nail images were excluded in the final leakage audit. The 1,563-image set above is used for the final experiment tables and reported results.

## Data handling

Raw pediatric images are not stored in this repository. Download them from the original records and observe source license, ethics, and privacy conditions. Do not upload subject identifiers or private/identifiable data.
