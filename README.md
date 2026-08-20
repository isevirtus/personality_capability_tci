# Replication Package: Personality, Capabilities, and Perceived Agile-Team Climate

This repository contains the data, questionnaire materials, and supplementary analyses for an empirical study of associations between personality traits, behavioral capabilities, and individual perceptions of agile-team climate in a Brazilian software organization. It also documents robustness checks for the regression analyses and a cross-context measurement-invariance assessment of the Team Climate Inventory (TCI).

## Study overview

The Brazilian study involved 148 professionals from 16 agile teams. The questionnaire covered:

- personality traits measured with the 120-item IPIP-NEO;
- five single-item capability measures: Responsibility, Listening Skills, Questioning Skills, Team Participation, and Teamwork Orientation; and
- perceived team climate measured with the 38-item TCI: Team Vision, Task Orientation, Support for Innovation, and Participative Safety.

The primary analyses use Spearman correlations and the manual stepwise regression procedure followed in the replicated study. The supplementary analyses include simultaneous-entry regression models, bootstrap stability checks, and a multigroup confirmatory factor analysis of the TCI across Brazil, Sweden, and India.

## Repository contents

| Path | Description |
|---|---|
| `data/data_raw.xlsx` | Original Brazilian dataset distributed with the study artifact. |
| `data/data_treated.xlsx` | Processed Brazilian dataset used in the reported analyses. |
| `instruments/questionnaires.pdf` | Questionnaire materials used for data collection. |
| `supplementary/S1_full_entry_regression_models.md` | Browser-readable version of the simultaneous-entry regression sensitivity analysis. |
| `supplementary/S2_tci_measurement_invariance.md` | Browser-readable version of the cross-context TCI measurement-invariance analysis. |
highlighted. |

## Supplementary analyses

### S1: Full-entry regression models

All ten personality and capability predictors were entered simultaneously for each outcome. This analysis provides an unselected specification against which the predictor pattern from the primary manual stepwise procedure can be compared.

### S2: Cross-context TCI measurement invariance

The 38 TCI items were evaluated across the Brazilian (`n = 148`), Swedish (`n = 75`), and Indian (`n = 46`) samples (`N = 269`) using multigroup confirmatory factor analysis with Robust Diagonally Weighted Least Squares estimation. Configural, metric, and scalar models were compared using the change in CFI. The results showed no detected TCI non-invariance under the adopted specification and criterion, subject to the limitations documented in Supplementary Material S2.

This analysis concerns the TCI only. It does not establish cross-context measurement invariance for the IPIP-NEO personality dimensions or the single-item capability measures, and it does not isolate national context from organizational, domain, sampling, or temporal differences among the studies.

## Using the materials

The current package supports inspection of the study data, instruments, and reported supplementary results. Executable analysis scripts are not included in this release. Users seeking to reproduce the analyses should consult the methodological descriptions in the manuscript and supplementary materials and verify that the final public release documents all software, preprocessing, missing-data, and model-identification decisions.

## Ethical use

The materials are provided for research and replication. Users must not attempt to identify participants or organizations from the shared data, combine the files with external information for re-identification, or use the data in ways inconsistent with the original consent and applicable ethics requirements.

## License

Unless otherwise noted, the data and documentation are released under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/), consistent with the prior artifact release. Any third-party instruments remain subject to their original terms of use.

## Contact

Questions about the package can be submitted through the repository's issue tracker.
