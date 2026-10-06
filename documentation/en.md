<!-- ELUCENIA technical documentation · escore-de-rockall · en · no clinical/professional/rights approval -->

# Rockall score

[conditions, sources and permissions](https://elucenia.org/en/tools/escore-de-rockall)

## How to use

Use the tool in the portal or open index.html through a local HTTP server. Select the language, complete the fields and calculate.

## Inputs and units

### Age

`idade`

- `0` — \< 60 years
- `1` — 60 to 79 years
- `2` — ≥ 80 years

### Shock

`choque`

- `0` — No shock (systolic blood pressure ≥ 100 and heart rate \< 100)
- `1` — Tachycardia (systolic blood pressure ≥ 100 and heart rate ≥ 100)
- `2` — Hypotension (systolic blood pressure \< 100 mmHg)

### Comorbidities

`comorb`

- `0` — None significant
- `2` — Heart failure, ischemic heart disease or other significant comorbidity
- `3` — Renal failure, liver failure or disseminated cancer

### Endoscopic diagnosis

`diag`

- `0` — Mallory-Weiss or no lesion (no stigmata)
- `1` — All other diagnoses
- `2` — Upper gastrointestinal neoplasm
- `na` — Endoscopy not yet performed

### Stigmata of recent bleeding

`estigma`

- `0` — None or dark spot only (hematin)
- `2` — Blood in the upper gastrointestinal tract, adherent clot, visible vessel or spurting bleeding
- `na` — Endoscopy not yet performed

## Method edition

Rockall 1996: pre-endoscopic 0–7 and complete 0–11; distinct from GBS

## Documented formula

Pre-endoscopic (0 to 7): age (0 to 2) + shock (0 to 2) + comorbidities (0, 2 or 3).

Complete (0 to 11): also adds diagnosis (0 to 2) and stigmata of recent bleeding (0 or 2).

## Limits and population

The 1996 Rockall was studied in people older than 16 years with acute upper gastrointestinal bleeding. The full version depends on the diagnosis and endoscopic stigmata; the pre-endoscopic version lacks that information. Stratification helps consider management but does not determine individual discharge safety or absence of rebleeding.

## References

- [Rockall TA et al. Risk assessment after acute upper gastrointestinal haemorrhage. Gut, 1996.](https://doi.org/10.1136/gut.38.3.316)

- [Stanley AJ et al. Comparison of risk scoring systems for patients presenting with upper gastrointestinal bleeding: international multicentre prospective study. BMJ, 2017.](https://doi.org/10.1136/bmj.i6432)

## Reproduce the technical tests

Run node test.cjs in the root directory of this repository to repeat the recorded synthetic cases. Original inputs, expectations and tolerances are preserved. Technical tests do not constitute clinical validation.

```sh
node test.cjs
```

tool.json contains sources, edition and review scope. examples.json retains synthetic inputs and expectations; results.json records the obtained results.

[Record and references](../tool.json) · [JavaScript code](../calculator.js) · [Reference cases](../examples.json) · [results.json](../results.json)

## Review and conditions of use

Independent clinical review has not been performed.

This interface is an authorial translation, not an official or certified edition. Independent clinical review, professional language review and instrument rights clearance have not been performed.

Formula or classification result. Interpretation, care and applicability depend on professional assessment and the selected source.

## License and attribution

Apache-2.0 applies only to ELUCENIA code. Rights to instruments, publications, translations and data remain with their respective holders. Preserve LICENSE and NOTICE.

ELUCENIA · Felipe Guedes · Copyright © 2026

## Documented results

The information below preserves the method outputs for synthetic examples. It does not constitute independent clinical validation.

### 1

Pre-endoscopic Rockall 0: low risk

Complete with the diagnosis and stigmata after endoscopy for the full score.


### 2

Pre-endoscopic Rockall ≥ 4: increased risk of death

Complete with the diagnosis and stigmata after endoscopy for the full score.


### 3

Complete Rockall ≤ 2: low risk of rebleeding and death

| Result details | |
| --- | --- |
| Pre-endoscopic part | 1 points |


### 4

Complete Rockall from 3 to 4: intermediate risk

| Result details | |
| --- | --- |
| Pre-endoscopic part | 4 points |


### 5

Complete Rockall ≥ 5: high risk of death

| Result details | |
| --- | --- |
| Pre-endoscopic part | 7 points |

