# Early Life Environments and Adult Cardiometabolic Health

This repository contains code for the manuscript:

**Early life environments shape adult cardiometabolic health during rapid lifestyle change**

The analyses assess early life effects and evaluate developmental constraints and predictive adaptive response hypotheses using anthropological and biomedical data from the Orang Asli of Peninsular Malaysia.

---

## Requirements

- **R version:** 4.5.1
- Package versions are recorded using renv (see renv.lock)
- A Google Maps API key (for geocoding via ggmap)
- Access to the protected data file hosted on Zenodo (https://zenodo.org/records/15684749): `Orang_Asli_data_file_for_Github.txt`

---

## Setting Up the Environment

Place the following files in the **same working directory**:

- `Early_life_effects_health_OA.Rmd`
- `renv.lock`
- `Orang_Asli_data_file_for_Github.txt` (protected data file)

No additional folder structure is required. 

Start a clean R session and restore the package environment by running the following:

```r
install.packages("renv")
renv::restore()
```

To set your Google Maps API key (required for geocoding) add the following line to your `.Renviron` file:

```r
GOOGLE_API_KEY=your_key_here
```

Then restart R. 

Exact session details (R version, platform, and loaded package versions) are provided in the `sessionInfo()` output at the end of the R Markdown document.

---

## Data Requirements

The analyses require a single input file: `Orang_Asli_data_file_for_Github.txt`

All preprocessing, variable coding, transformation, statistical modelling, principal components analysis, and figure generation are performed within `Early_life_effects_health_OA.Rmd`. No additional preprocessing steps are required. Current urbanicity scores are included directly in the provided data file. The script used to generate this location-based urbanicity score is available separately at:

https://github.com/mwatowich/Multi-population_lifestyle_scales/blob/main/scripts/lifestyleScale_locationAggregateUrbanicity.R

The output of that script is what is included in `Orang_Asli_data_file_for_Github.txt`. Re-running that script is **not required** to reproduce the analyses in this repository.

---

## Data Access

The associated data are housed on Zenodo (https://zenodo.org/records/15684749) and are available through restricted access. Requests for de-identified, individual-level data must include:
- A detailed description of research questions and proposed analyses
- Data security and privacy procedures
- Consideration of potential benefits to study communities
- Procedures for assessing and minimizing stigmatizing interpretations
- Institutional IRB approval (even if exempt)

OA HeLP is committed to open science and project leadership is available to assist investigators in preparing data access requests. For further details and contact information see the [OA HeLP website](https://orangaslihealth.org).


