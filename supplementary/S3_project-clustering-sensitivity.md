# Supplementary Material S3 — Sensitivity to Project-Level Clustering

## Objective and data structure

The primary analyses used the individual respondent as the unit of analysis. However, the 148 Brazilian respondents were associated with 22 projects, and respondents working on the same project could have reported correlated perceptions because they shared aspects of their work context. We therefore evaluated the magnitude of project-level dependence and whether accounting for this dependence materially changed the five focal associations retained by the primary regression procedure.

This analysis concerns clustering by project. It does not aggregate respondents' scores or estimate team- or project-level climate.

## Estimation

We first fitted an intercept-only linear mixed model for each outcome with a random intercept for project. We calculated ICC(1) as

\[
\mathrm{ICC}(1)=\frac{\tau_{00}}{\tau_{00}+\sigma^2},
\]

where \(\tau_{00}\) is the between-project variance and \(\sigma^2\) is the residual variance.

We then re-estimated each final Brazilian model as a linear mixed model containing the predictor retained by the primary procedure as a fixed effect and a random intercept for project. The models were estimated using restricted maximum likelihood (REML) in IBM SPSS Statistics version 25. We compared the fixed-effect coefficients, standard errors, confidence intervals, and significance levels with those from the primary respondent-level models.

ICC(2) and within-group agreement indices such as \(r_{wg}\) were not calculated because the study did not aggregate responses or claim to estimate a higher-level climate construct. Accordingly, this analysis quantifies project-related dependence but does not evaluate whether aggregation to the team or project level would be justified.

## Project-level dependence

### Table S3.1. ICC(1) estimates for the five perceived team-climate outcomes

| Outcome | Between-project variance (\(\tau_{00}\)) | Residual variance (\(\sigma^2\)) | ICC(1) | Wald Z \(p\) for \(\tau_{00}\) |
|---|---:|---:|---:|---:|
| Team Vision | 0.048 | 0.305 | .135 | .112 |
| Task Orientation | 0.141 | 0.339 | .294 | .021 |
| Support for Innovation | 0.162 | 0.425 | .276 | .024 |
| Participative Safety | 0.155 | 0.387 | .286 | .020 |
| IPTC | 0.122 | 0.261 | .319 | .017 |

The ICC(1) estimates ranged from .135 to .319. Thus, the intercept-only models attributed approximately 14% to 32% of the variance in respondents' outcome scores to differences between projects. The estimated between-project variance had a Wald Z \(p\)-value below .05 for four of the five outcomes; the exception was Team Vision (\(p=.112\)). These results indicate non-negligible project-related dependence, although variance-component tests and estimates should be interpreted cautiously given the 22 project clusters.

## Random-intercept sensitivity models

### Table S3.2. Fixed-effect estimates from models with a random intercept for project

| Outcome | Fixed-effect predictor | \(B\) | SE | 95% CI | \(p\) | Conditional ICC(1) |
|---|---|---:|---:|---:|---:|---:|
| Team Vision | Responsibility | 0.388 | 0.094 | [0.202, 0.574] | < .001 | .145 |
| Task Orientation | Agreeableness | 0.007 | 0.002 | [0.003, 0.011] | .001 | .295 |
| Support for Innovation | Agreeableness | 0.008 | 0.002 | [0.004, 0.013] | < .001 | .280 |
| Participative Safety | Agreeableness | 0.007 | 0.002 | [0.003, 0.011] | .002 | .286 |
| IPTC | Agreeableness | 0.006 | 0.002 | [0.003, 0.010] | < .001 | .326 |

All five focal fixed-effect estimates retained the same direction and remained statistically significant after a random intercept for project was included. None of the reported confidence intervals included zero. The conditional ICC(1) estimates remained close to those from the intercept-only models, indicating that the focal individual-level predictors accounted for little of the estimated between-project variation.

These results provide sensitivity evidence that the focal Brazilian associations were not eliminated when dependence associated with shared project context was modeled. They do not establish team- or project-level effects, demonstrate within-project agreement, identify the contextual characteristics responsible for between-project variation, eliminate unmeasured confounding, or support causal interpretation.

## SPSS syntax

The following syntax reproduces the five random-intercept sensitivity models. `projeto` is the project-grouping variable. Variable names are reproduced as used in the analytical dataset.

```spss
MIXED TeamVision WITH CAPAResponsibility
  /CRITERIA=CIN(95)
  /FIXED=CAPAResponsibility | SSTYPE(3)
  /METHOD=REML
  /PRINT=SOLUTION TESTCOV
  /RANDOM=INTERCEPT | SUBJECT(projeto) COVTYPE(VC).

MIXED TaskOrientation WITH Agreeableness
  /CRITERIA=CIN(95)
  /FIXED=Agreeableness | SSTYPE(3)
  /METHOD=REML
  /PRINT=SOLUTION TESTCOV
  /RANDOM=INTERCEPT | SUBJECT(projeto) COVTYPE(VC).

MIXED SupportForInovation WITH Agreeableness
  /CRITERIA=CIN(95)
  /FIXED=Agreeableness | SSTYPE(3)
  /METHOD=REML
  /PRINT=SOLUTION TESTCOV
  /RANDOM=INTERCEPT | SUBJECT(projeto) COVTYPE(VC).

MIXED ParticipativeSafety WITH Agreeableness
  /CRITERIA=CIN(95)
  /FIXED=Agreeableness | SSTYPE(3)
  /METHOD=REML
  /PRINT=SOLUTION TESTCOV
  /RANDOM=INTERCEPT | SUBJECT(projeto) COVTYPE(VC).

MIXED iptc WITH Agreeableness
  /CRITERIA=CIN(95)
  /FIXED=Agreeableness | SSTYPE(3)
  /METHOD=REML
  /PRINT=SOLUTION TESTCOV
  /RANDOM=INTERCEPT | SUBJECT(projeto) COVTYPE(VC).
```
