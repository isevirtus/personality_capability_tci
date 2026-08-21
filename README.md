# Replication Package: Personality, Capabilities, and Perceived Agile-Team Climate

This repository contains the de-identified data, questionnaire materials, supplementary analyses, and selected statistical-software outputs associated with an empirical study of relationships among personality traits, self-reported behavioral capabilities, and professionals' perceptions of agile-team climate in a Brazilian software organization.

The package documents the primary respondent-level analyses, regression robustness checks, measurement assessment of the Team Climate Inventory (TCI), cross-context TCI measurement invariance, and sensitivity to project-level clustering.

## Study overview

The Brazilian sample comprised 148 professionals from 16 agile teams working across 22 projects. The individual respondent was the unit of analysis. TCI scores were calculated separately for each participant and were not aggregated into team- or project-level climate scores.

The questionnaire covered:

- personality traits measured using the 120-item IPIP-NEO;
- five single-item capability measures: Responsibility, Listening Skills, Questioning Skills, Team Participation, and Teamwork Orientation; and
- perceived team climate measured using the 38-item TCI: Team Vision, Task Orientation, Support for Innovation, and Participative Safety.

The primary analyses used Spearman correlations and the manual stepwise regression procedure followed in the replicated study. Complementary analyses included:

- simultaneous-entry models containing all ten personality and capability variables;
- a 5,000-sample case-resampling bootstrap stability assessment;
- Brazilian TCI reliability and confirmatory factor analysis;
- multigroup confirmatory factor analysis of the TCI across Brazil, Sweden, and India; and
- project random-intercept models assessing sensitivity to project-level clustering.

The comparisons among the Brazilian, Swedish, and Indian samples are qualitative. They do not isolate national culture from organizational, domain, linguistic, sampling, methodological, or temporal differences among the studies.

## Relationship to the previous Brazilian study

The personality and TCI data from the same 148 Brazilian professionals were previously analyzed in a personality–climate replication study. The present study extends that work by analyzing the previously unreported capability measures, estimating combined personality–capability models following the procedure used in the Swedish–Indian study, and qualitatively comparing the resulting patterns across the three settings.

The present package also includes measurement and sensitivity analyses that were not part of the previous Brazilian publication.

## Repository contents

| Path | Description |
|---|---|
| `data/data_raw.xlsx` | De-identified Brazilian item-level dataset before the transformations used to construct the analysis-ready variables. |
| `data/data_treated.xlsx` | Processed, analysis-ready Brazilian dataset used in the reported statistical analyses. |
| `instruments/questionnaires.pdf` | Questionnaire materials used during data collection. |
| `supplementary/S1_full_entry_regression_models.md` | Browser-readable report of the simultaneous-entry regression sensitivity analysis. |
| `supplementary/S2_tci_measurement_invariance.md` | Browser-readable report of the cross-context TCI measurement-invariance analysis. |
| `supplementary/S3_project_clustering_sensitivity.md` | Browser-readable report of the ICC(1) estimates and project random-intercept sensitivity models. |
| `software-output/cfa-tci-jasp-output.pdf` | Raw JASP output supporting the Brazilian TCI confirmatory factor analysis and reliability assessment. |
| `software-output/simultaneous-entry/` | Raw SPSS outputs for the five simultaneous-entry regression models. |
| `software-output/mixed-models-spss-output.pdf` | Consolidated SPSS output for the project random-intercept models. |
| `LICENSE` | License governing the repository materials, subject to the third-party instrument qualifications described below. |

Some raw SPSS outputs may use Portuguese interface labels because the analyses were conducted using a Portuguese-language installation. The English-language Markdown documents provide the reader-facing descriptions of the procedures, results, and limitations.

## Supplementary analyses

### S1: Simultaneous-entry regression models

All ten personality and capability variables were entered simultaneously into a separate model for each perceived team-climate outcome. This specification avoids the sequential inclusion and exclusion path of the primary manual stepwise procedure and allows every coefficient to be estimated while controlling for the other nine measured variables.

The simultaneous-entry models are presented as sensitivity analyses rather than as independently confirmatory models. Complete estimates, model-fit statistics, and relevant qualifications are reported in `supplementary/S1_full_entry_regression_models.md`.

### S2: Cross-context TCI measurement invariance

The 38 TCI items were evaluated across the Brazilian (`n = 148`), Swedish (`n = 75`), and Indian (`n = 46`) samples (`N = 269`) using multigroup confirmatory factor analysis with WLSMV estimation.

Configural, metric, and scalar models were fitted sequentially. Under the adopted model specification and comparison criterion, the results were consistent with configural, metric, and scalar invariance and did not indicate TCI measurement non-invariance across the three samples.

This result should be interpreted as an absence of detected TCI non-invariance under the tested specification and criterion, rather than as conclusive proof of complete measurement equivalence. The complete procedure, fit indices, preprocessing decisions, diagnostics, and limitations are reported in `supplementary/S2_tci_measurement_invariance.md`.

The analysis concerns only the TCI. It does not establish cross-context measurement invariance for the IPIP-NEO personality dimensions or the single-item capability measures.

### S3: Sensitivity to project-level clustering

Because the 148 Brazilian respondents were associated with 22 projects, intercept-only linear mixed models were used to estimate project-level ICC(1) values for the five perceived team-climate outcomes. The estimates ranged from `.135` to `.319`, indicating non-negligible project-related dependence.

The five focal Brazilian models were subsequently re-estimated with a random intercept for project. The focal fixed-effect estimates retained their direction and remained statistically significant after project-related dependence was modeled.

These results provide sensitivity evidence concerning the respondent-level associations. They do not establish team- or project-level effects, demonstrate within-project agreement, justify aggregation, eliminate unmeasured confounding, or support causal conclusions. Complete results and SPSS syntax are provided in `supplementary/S3_project_clustering_sensitivity.md`.

### Bootstrap stability assessment

The manuscript additionally reports a case-resampling bootstrap analysis using 5,000 samples with replacement. Bootstrap confidence intervals were calculated for the five focal coefficients, and the full ten-variable model was fitted in each bootstrap sample to estimate how frequently each focal coefficient reached `p < .05`.

The results generally supported the focal associations, although the Agreeableness–Task Orientation association showed comparatively lower bootstrap stability. This analysis evaluates sensitivity to sampling variation but is not a formal familywise-error correction.

## Software

The analyses were conducted using:

- **IBM SPSS Statistics 25** for the primary regressions, simultaneous-entry models, bootstrap analyses, and project random-intercept models; and
- **JASP 0.98.1**, through its implementation of the `lavaan` package, for the factor analyses.

The factor analyses used WLSMV estimation for ordinal items. Additional model-identification, preprocessing, and comparison details are documented in the relevant supplementary materials.

## Using the materials

The package supports inspection of the study data, instruments, reported supplementary results, and selected raw software outputs. It is not presented as a fully executable end-to-end reproduction pipeline because complete standalone analysis scripts are not available for every reported analysis.

Users seeking to reproduce or extend the analyses should consult:

1. the methodological descriptions in the manuscript;
2. the browser-readable supplementary reports;
3. the included SPSS syntax where available; and
4. the corresponding raw statistical-software outputs.

Differences in software versions, defaults, missing-data handling, estimator implementation, or preprocessing may affect reproduced results.

## Data protection and ethical use

Only de-identified materials suitable for public release should be included in this repository. Before publishing any dataset or software-output file, the authors should verify that it contains no participant names, real project names, organizational identifiers, usernames, local file paths, or other information that could facilitate re-identification.

The materials are provided for research and replication. Users must not attempt to identify participants, projects, teams, or organizations; combine the files with external information for re-identification; or use the data in ways inconsistent with the original consent and applicable ethics requirements.

## License

Unless otherwise noted, the data and original documentation are released under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

Third-party instruments and associated item wording remain subject to their original copyright, licensing, and terms-of-use conditions. Inclusion in this repository does not relicense third-party materials under CC BY 4.0.

## Contact

Questions about the replication package can be submitted through the repository's issue tracker.
