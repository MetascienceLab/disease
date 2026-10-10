# Distinct Roles of Different Funding Structures in the Impact of U.S. Disease Research

This folder contains selected analysis code associated with the manuscript. It is a code disclosure package, not a complete runnable copy of the private research workspace. The source notebooks were inspected and excerpted without executing their cells. The copies here have no saved cell outputs.

## Contents

| File | Manuscript connection |
| --- | --- |
| `notebooks/01_cohort_and_funding.ipynb` | PubMed and MeSH screening, matching to WoS, funding extraction, and publication-level funding and disease labels (Data and Methods). |
| `notebooks/02_main_models.ipynb` | Impact indicators, citation inputs, control matching, and academic, policy, patent, and clinical regression code (Figure 2, Figure 3, Table 1, and Supplementary Table S3). |
| `notebooks/03_manuscript_figures.ipynb` | Selected code for funding composition, disease-area comparisons, disease-specific impact, research orientation, and funder subtypes (Figures 1, 3, and 4). |
| `notebooks/04_robustness.ipynb` | Code for excluding 2022, checking small disease areas, restricting to two funders, and validating agency classifications (supplementary analyses). |
| `notebooks/05_agency_classification_v2.ipynb` | GPT-5 mini v2 prompts and code for classifying agency type and U.S. status, plus the validation calculation. |
| `agency_classification_validation_1000.csv` | GPT-5 mini v2 labels and manual labels for the same 1,000 sampled agencies. Names, aliases, and source frequencies are omitted. |
| `mesh_lvl1_disease_mapping.csv` | The 24-row MeSH category-name lookup used in disease-area analyses. |

The notebooks are organized by research step. Each section explains its purpose and the relevant inputs or outputs. Some code cells depend on intermediate variables created in other cells or on restricted input files. This package documents the analysis methods; it cannot reproduce every numerical result by itself.

## Data access and limits

The analysis uses PubMed Knowledge Graph / PubMed, Web of Science (WoS), Overton, Global Burden of Disease, OpenAlex, and linked patent and clinical-trial data. The WoS files were provided through institutional access and are **not distributed here**. This folder also excludes WoS-derived publication-level records, funding acknowledgments, matched identifiers, intermediate data, model output tables, and figure-ready regression results. The complete manuscript estimates cannot be recomputed from this folder alone.

The agency validation file contains 1,000 rows of category and country labels with sequential IDs; it contains no agency names, aliases, frequencies, or publication identifiers. The second data file is a 24-row disease-category lookup. Any later sample release should be separately reviewed for source rights and capped at 1,000 rows.

The agency validation sample matches the manual coding described in the manuscript. GPT-5 mini v2 agreed with the manual agency-type labels for 921 of 1,000 organizations (92.1%) and with the manual U.S./non-U.S. labels for 911 of 1,000 (91.1%). The full set of 61,452 classified organization records is not distributed.

## Notes for readers

- Figures and tables in the manuscript were produced from the full analytical data, not from the category lookup in this folder.
- The folder does not include environment-specific paths, API keys, passwords, saved notebook outputs, or research data dumps. The GPT-5 mini code expects the API key in `OPENAI_API_KEY` and a separately authorized agency input file.
- Some original plotting cells embedded model estimates as literal values. Those cells and all result tables have been omitted in line with this repository's code-only scope.
- Data source versions, access conditions, and the cohort definition are described in the manuscript's Data and Methods section.

