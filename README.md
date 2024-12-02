# Data of the SuperIce project
This repository contained an updated description of the data produced in the SuperIce project led by the [NERSC](https://nersc.no/) and supported by [ESA Φ-lab](https://philab.esa.int/)

More info on the project: (link to the website)[https://nansencenter.github.io/superice-nersc/]

## Download instruction
Data are stored on the https://archive.sigma2.no/ archive.

## tree of the data
The data is stored under the following paths:

```
model/
├── feature/
└── prediction/

observations/
├── feature/
└── prediction/
```

## Description of subsets

**1.  `model/feature`**

Contains pairs of low-resolution/high-resolution fields from the NeXtSIM simulation. The dataset generation is described in this document. The fields are listed here
| Variable               | Description                              |
|------------------------|------------------------------------------|
| `time`                 | Time in days since 2022-01-12 00:00:00   |
| `longitude`            | Longitude in degrees east                |
| `latitude`             | Latitude in degrees north                |
| `sic`                  | Sea Ice Concentration                    |
| `sic_reprocessed`      | Reprocessed Sea Ice Concentration        |
| `sit`                  | Sea Ice Thickness                        |
| `sit_reprocessed`      | Reprocessed Sea Ice Thickness            |
| `divergence`           | Divergence of sea ice motion             |
| `divergence_reprocessed` | Reprocessed Divergence of sea ice motion |
| `shear`                | Shear of sea ice motion                  |
| `shear_reprocessed`    | Reprocessed Shear of sea ice motion      |

the `*_reprocessed` fields are the actual input feature, consisting in low-resolution fields. The other fields `sic`, `sit`, `divergence`, and `shear` can be used as ground truth or labels and are not observable by satellite.
