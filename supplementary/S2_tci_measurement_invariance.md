# Supplementary Material S2 — Cross-Context Measurement Invariance of the Team Climate Inventory

## Objective and samples

We assessed whether the 38-item Team Climate Inventory (TCI) operated comparably across the Brazilian (`n = 148`), Swedish (`n = 75`), and Indian (`n = 46`) samples (`N = 269`). The original four-factor structure was specified in each group: Team Vision (11 items), Task Orientation (7 items), Support for Innovation (8 items), and Participative Safety (12 items).

## Software, preprocessing, and estimation

The analyses were conducted in JASP version 0.98.1 (July 6, 2026), using the `lavaan` package. Model identification and scaling followed the default JASP/`lavaan` implementation. Because the TCI items are ordinal, the models were estimated using Weighted Least Squares Mean and Variance Adjusted (WLSMV) estimation, following Brown (2015).

The TCI items were administered using a five-point response scale. During preparation of the data for the multigroup analysis, some response categories were unobserved for some items in at least one national sample. The affected items were therefore represented using four ordered response categories for the MGCFA.

## Model comparisons

Configural, metric, and scalar models were fitted sequentially. The configural model retained the same four-factor pattern across groups, the metric model constrained the factor loadings across groups, and the scalar model added equality constraints on the item thresholds. A decrease in CFI greater than .01 was treated as evidence against invariance, following Cheung and Rensvold (2002).

## Results

### Table S2. Multigroup CFA of the TCI across Brazil, Sweden, and India (`N = 269`)

| Measurement-invariance model | RMSEA (90% CI) | SRMR | TLI | CFI | ΔCFI |
|---|---:|---:|---:|---:|---:|
| Configural | .080 [.075, .086] | .104 | .939 | .943 | — |
| Metric (equal loadings) | .073 [.068, .079] | .111 | .949 | .951 | +.008 |
| Scalar (equal thresholds) | .076 [.070, .081] | .104 | .946 | .944 | −.007 |

The configural model showed acceptable but not strong fit: CFI and TLI exceeded .90 without reaching .95, RMSEA was at the upper recommended bound, and SRMR exceeded the conventional threshold. Adding the metric and scalar constraints did not produce a decrease in CFI greater than .01. Under the adopted criterion, the results were therefore consistent with metric and scalar invariance of the TCI across the three samples.

## Diagnostics and limitations

Three qualifications constrain this conclusion.

1. The full model estimated 474 free parameters from 269 respondents, producing an unfavorable parameter-to-sample ratio. The Indian sample showed the largest median standard errors for the loadings (.294, compared with .187 in Brazil and .260 in Sweden), although no Heywood cases or negative residual variances occurred in any group.

2. Item `tv11` showed a standardized loading close to unity with a large standard error in the Brazilian sample, indicating local empirical underidentification and corresponding to negligible negative eigenvalues in the parameter covariance matrix.

3. Some items were represented using four ordered response categories rather than the original five categories to permit estimation of the multigroup model. This preprocessing decision may have reduced measurement resolution. The moderate country-specific sample sizes, particularly the Indian sample, also limited the sensitivity of the analysis to detect non-invariance.

The results should therefore be interpreted as an absence of detected TCI measurement non-invariance under the tested specification and criterion, rather than as conclusive proof of complete measurement equivalence. The analysis applies only to the TCI and does not establish cross-context measurement invariance for the personality traits or the single-item capability measures.
