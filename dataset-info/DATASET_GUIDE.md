# Dataset guide

## Source records

The study uses the following three Mendeley Data records, as identified in the experiment notebooks:

| Site | DOI | Local folder |
|---|---|---|
| Palm | [10.17632/ccr8cm22vz.1](https://doi.org/10.17632/ccr8cm22vz.1) | `Dataset_Multisite/Palm/` |
| Nail | [10.17632/2xx4j3kjg2.1](https://doi.org/10.17632/2xx4j3kjg2.1) | `Dataset_Multisite/Nail/` |
| Conjunctiva | [10.17632/nt7r8hv2pz.1](https://doi.org/10.17632/nt7r8hv2pz.1) | `Dataset_Multisite/Conjunctiva/` |

The experiment notebooks describe these source records as CC BY 4.0. Check the current record page and its license statement before reuse or redistribution.

## Expected local layout

```text
Dataset_Multisite/
├── Palm/
│   ├── Anemic-...
│   └── Non-Anemic-...
├── Nail/
│   ├── Anemic-...
│   └── Non-Anemic-...
└── Conjunctiva/
    ├── Anemic-...
    └── Non-Anemic-...
```

Keep the source filenames unchanged. The notebooks infer labels from the `Anemic` and `Non-Anemic` filename prefixes and sort filenames before processing. Some copies and variants are handled by the audit/cleaning functions; do not manually rename files unless you also document the change.

## Cleaning definition used in the study

The clean data definition in the notebooks removes (1) duplicate images identified by MD5 while retaining one copy, (2) both members of an identical-image pair with conflicting labels, and (3) detected variant files when their base image exists. The resulting clean collection reported in the manuscript contains 1,345 images: Palm 519, Nail 312, and Conjunctiva 514.

## Data handling

Raw pediatric images are not stored in this GitHub repository. Download them from the original data records and observe the source license, ethics, and privacy conditions. Do not upload subject identifiers or private/identifiable data to this repository.
