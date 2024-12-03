# Data of the SuperIce project
This repository contained an updated description of the data produced in the SuperIce project led by the [NERSC](https://nersc.no/) and supported by [ESA Φ-lab](https://philab.esa.int/)

More info on the project: (link to the website)[https://nansencenter.github.io/superice-nersc/]

## Download instruction
Data are stored on the https://archive.sigma2.no/ archive.

## tree of the data
The data is stored under the following paths:

```
model/
├── features/
└── predictions/

observations/
├── features/
└── predictions/
```

## Description of subsets

**1.  `model/features`**

File format: `YYYYMMDD.nc` (`YYYY`: year, `MM`: month, `DD`: day in the month)

Time Period: From 2020 to 2023, only the freezing season (18 Oct. to 15 Apr.)

Contains pairs of low-resolution/high-resolution fields from the NeXtSIM simulation. The dataset generation is described in this document. The fields are listed here
## Variables
Dimensions: y = 1086 ; x = 1308

| Variable               | Dimensions  | Description                              |
|------------------------|-------------|------------------------------------------|
| `time`                 | -           | Time in days since 2022-01-12 00:00:00   |
| `longitude`            | (y, x)    | Longitude in degrees east                |
| `latitude`             | (y, x)    | Latitude in degrees north                |
| `sic`                  | (y, x)    | Sea Ice Concentration                    |
| `sic_reprocessed`      | (y, x)    | Reprocessed Sea Ice Concentration        |
| `sit`                  | (y, x)    | Sea Ice Thickness                        |
| `sit_reprocessed`      | (y, x)    | Reprocessed Sea Ice Thickness            |
| `divergence`           | (y, x)    | Divergence of sea ice motion             |
| `divergence_reprocessed` | (y, x)  | Reprocessed Divergence of sea ice motion |
| `shear`                | (y, x)    | Shear of sea ice motion                  |
| `shear_reprocessed`    | (y, x)    | Reprocessed Shear of sea ice motion      |



the `*_reprocessed` fields are the actual input feature, consisting in low-resolution fields. The other fields `sic`, `sit`, `divergence`, and `shear` can be used as ground truth or labels and are not observable by satellite.



