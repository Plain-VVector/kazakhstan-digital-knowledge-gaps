# Kazakhstan Digital Knowledge Gaps: Replication Package
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22712068.svg)](https://doi.org/10.5281/zenodo.22712068)

**Archived release v1.0.1:** https://doi.org/10.5281/zenodo.22712068  
**DOI for all versions:** https://doi.org/10.5281/zenodo.22695029
**Release:** v1.0.1
**Status:** Frozen research release
**Purpose:** Replication materials for a study of digital knowledge gaps related to Kazakhstan across Kazakh Wikipedia, Wikidata, and large language models.

## Overview

This release contains the datasets and final analytical outputs used in the study. It is preserved as a fixed research snapshot so that the reported results can be reproduced independently of later changes to Wikidata, Wikipedia, the Digital Gap Detector, or AI systems.

The release contains **34 research data and result files**, together with `manifest_release_v1.0.1.json`, which records file names, sizes, and SHA-256 hashes.

Two different analytical populations are used in the study and should not be confused:

`kkwiki_analytical_corpus.csv` contains the broader Kazakh Wikipedia corpus used for structural and article-depth analyses.

`kazakhstan_territorial_universe.csv` contains the Wikidata-derived universe of entities associated with the territory of Kazakhstan and is used to examine knowledge coverage and missing Kazakh Wikipedia articles.

## 1. Kazakh Wikipedia corpus and article structure

`kkwiki_analytical_corpus.csv`  
Final article-level analytical corpus containing **244,411 pages** and structural metrics such as article length, word count, references, images, internal links, and categories. The initial analytical corpus contained 245,200 pages; an additional 789 pages classified in Wikidata as `Q4167410` (*Wikimedia disambiguation page*) were excluded before the final corpus was frozen.

`kkwiki_p31.csv`
Links Kazakh Wikipedia articles to Wikidata instance-of (`P31`) classes.

`p31_labels_verified.csv`
Verified labels for Wikidata P31 classes used in the analysis.

`kkwiki_thematic_depth.csv`
Aggregated article-depth indicators by thematic/P31 class.

`kkwiki_standardization_by_p31.csv`
Measures of within-class structural similarity and standardization.

`kkwiki_creator_summary.csv`
Aggregated distribution of article creation across identified creators. Individual-level creator records are not included in this public release.

## 2. Kazakhstan coverage and Wikidata analysis

`kazakhstan_territorial_universe.csv`
Research universe of Wikidata entities associated with Kazakhstan, including whether a corresponding Kazakh Wikipedia article exists.

`kazakhstan_p31_universe_final_detail.csv`
Entity-level P31 coverage data.

`kazakhstan_p31_universe_final_summary.csv`
Aggregated coverage and missing-article statistics by P31 class.

`kazakhstan_p31_class_coverage_exploded.csv`
Class-level coverage indicators and cross-language Wikipedia presence.

`kazakhstan_external_gap_p31_master.csv`
Final class-level dataset describing external knowledge gaps.

`wikipedia_wikidata_master_results_v1.0.csv`
Consolidated final results from the Wikipedia and Wikidata analyses.

`wikipedia_wikidata_master_manifest_v1.0.json`
Manifest associated with the consolidated Wikipedia/Wikidata results.

## 3. Gender representation and article depth

`kazakhstan_human_gender_final.csv`
Gender classification and Kazakh Wikipedia coverage for human entities in the Kazakhstan-related dataset.

`kazakhstan_gender_depth.csv`
Summary article-depth statistics by gender.

`gender_depth_continuous_tests.csv`
Statistical comparisons of continuous article-depth indicators.

`gender_depth_categorical_tests.csv`
Statistical comparisons of categorical article-depth indicators.

## 4. AI benchmark

The AI benchmark compares matched entities with and without Kazakh Wikipedia coverage. It includes recognition tasks and factual questions.

`ai_benchmark_recognition_scoring_FINAL_UNBLINDED_v1.1.csv`
Final unblinded recognition scoring dataset.

`recognition_primary_mcnemar_v1.1.csv`
Primary paired recognition comparison using the exact McNemar test.

`recognition_primary_bootstrap_ci_v1.1.csv`
Paired bootstrap confidence intervals for recognition differences.

`recognition_ambiguous_sensitivity_v1.1.csv`
Prespecified sensitivity analysis for ambiguous recognition cases.

`recognition_by_class_descriptive_v1.1.csv`
Descriptive recognition results by entity class.

`ai_benchmark_factual_scoring_FINAL_UNBLINDED_v1.0.csv`
Final unblinded factual-question scoring dataset.

`factual_results_overall_descriptive_v1.0.csv`
Overall descriptive factual accuracy results.

`factual_results_overall_cluster_inference_v1.0.csv`
Primary factual inference using cluster bootstrap confidence intervals and cluster permutation tests. Clustering preserves the original matched entity-pair structure.

`factual_results_by_property_v1.0.csv`
Factual results by Wikidata property.

`factual_results_by_class_property_v1.0.csv`
Factual results by entity class and property.

`factual_secondary_sensitivity_overall_v1.0.csv`
Overall prespecified factual sensitivity analysis.

`factual_secondary_sensitivity_by_property_v1.0.csv`
Prespecified sensitivity results by property.

`factual_nonanswer_overall_v1.0.csv`
Overall non-answer rates.

`factual_nonanswer_by_property_v1.0.csv`
Non-answer rates by property.

`factual_nonanswer_cluster_inference_v1.0.csv`
Cluster-based inference for non-answer differences.

`ai_benchmark_master_results_v1.0.csv`
Consolidated final AI benchmark results.

`ai_benchmark_master_results_v1.0.json`
Machine-readable manifest and metadata for the consolidated AI benchmark results.

## Reproducibility

This directory represents a frozen research release. Files in this release should not be modified after publication.

The live Digital Gap Detector may use newer versions of Wikidata- and Wikipedia-derived data. Such updates do not replace or modify this research snapshot.

`manifest_release_v1.0.1.json` provides SHA-256 hashes that can be used to verify that the released files have not changed.

A cleaned reproduction notebook and software environment information will accompany the final public release.

## Data provenance

The study uses data derived from Wikimedia projects, including Wikidata and Kazakh Wikipedia, together with research-generated analytical datasets and AI benchmark outputs.

The underlying Wikimedia projects remain subject to their respective licensing and attribution requirements.

## Citation

A DOI and recommended citation will be added after the archival release is deposited.

## Version

**v1.0** - Frozen dataset corresponding to the reported study results.

<!-- REPRODUCIBILITY_START -->

## Reproducibility

Release v1.0.1 is a frozen replication package. It is independent of the
live Digital Gap Detector, whose underlying product data may be updated
as Wikipedia and Wikidata change.

The principal frozen datasets reproduce the following reference values:

- final Kazakh Wikipedia analytical corpus: **244,411 pages**;
- pages with Wikidata QID: **241,506 (98.81%)**;
- Kazakhstan-related Wikidata universe: **29,521 entities**;
- entities with a Kazakh Wikipedia article: **17,866 (60.52%)**;
- entities without a Kazakh Wikipedia article: **11,655 (39.48%)**.

The corrected human-gender reference dataset contains **6,479 entities**.
For the binary P21 groups, Kazakh Wikipedia coverage is:

- Female: **529 / 1,505 (35.15%)**;
- Male: **2,195 / 4,725 (46.46%)**.

The frozen biography-depth comparison contains **220 female** and
**962 male** articles.

### AI benchmark

The AI benchmark compares matched entities with and without Kazakh
Wikipedia coverage. Frozen scored model outputs are distributed with
this release; reproduction does **not** require sending new prompts to
the model providers.

The evaluated models are:

- **GPT-5.6 Terra**
- **Gemini 3.6 Flash**

For the primary entity-recognition endpoint, each model was evaluated
on **126 matched entity pairs**. Statistical inference used:

- exact McNemar test;
- paired pair-bootstrap 95% confidence interval;
- **20,000 bootstrap resamples**;
- random seed `20260902`.

For the primary factual endpoint, the dataset contains **143 matched
pair-property tests** derived from **99 original matched entity pairs**.
Because some entity pairs contribute more than one factual property,
overall inference preserves the original entity-pair clustering:

- **100,000 cluster-bootstrap resamples** for the 95% confidence interval;
- **200,000 cluster permutations** for the two-sided permutation test;
- cluster = original matched entity pair;
- random seed `20260902`.

The four primary comparisons reproduced from the frozen scoring data are:

| Benchmark | Model | Covered | Missing | Difference | 95% CI | p |
|---|---|---:|---:|---:|---:|---:|
| Recognition | GPT-5.6 Terra | 31.75% | 27.78% | +3.97 pp | -5.56 to +12.70 pp | 0.4996 |
| Recognition | Gemini 3.6 Flash | 42.86% | 42.06% | +0.79 pp | -8.73 to +10.32 pp | 1.0000 |
| Factual | GPT-5.6 Terra | 47.55% | 48.25% | -0.70 pp | -8.51 to +7.75 pp | 1.0000 |
| Factual | Gemini 3.6 Flash | 58.74% | 57.34% | +1.40 pp | -5.63 to +8.39 pp | 0.8446 |

None of the four primary covered-versus-missing comparisons reached
the conventional 0.05 significance threshold, and all four 95%
confidence intervals include zero.

### Running the reproduction notebook

The main reproducibility entry point is:

`analysis_reproduction.ipynb`

Install the frozen Python dependencies with:

    pip install -r requirements.txt

The final verification environment used:

- Python 3.13.15
- NumPy 2.1.3
- pandas 2.2.3
- SciPy 1.16.3
- IPython 7.34.0
- nbformat 5.11.1
- nbclient 0.10.4

The clean release notebook contains no saved outputs or execution
counts. Running it from the release directory reproduces the principal
Wikipedia/Wikidata, gender, and AI benchmark results and checks them
against the frozen result tables.

### Data timing

The Kazakh Wikipedia dump files used to construct the analytical corpus
were retrieved on **23 August 2026** from Wikimedia's `latest` dump
endpoints. Because the source URL used the `latest` alias, this date is
reported as the **retrieval date**, not as an independently verified
internal Wikimedia snapshot date.

All research datasets in release v1.0.1 are frozen. Subsequent changes to
Wikipedia, Wikidata, model services, or the live Digital Gap Detector do
not modify this release.

### Integrity

`manifest_release_v1.0.1.json` contains SHA-256 hashes for the frozen
release files. The manifest must be regenerated after all publication
metadata files are finalized and immediately before publication.

<!-- REPRODUCIBILITY_END -->

<!-- PROVENANCE_NOTICE -->

## Licensing and provenance

The author's original contribution to this replication package is
released under **CC0 1.0 Universal**, to the extent that the author
holds the relevant copyright, database, or related rights.

Third-party and pre-existing content is not relicensed by this
dedication and remains subject to its original rights and terms.
See `PROVENANCE.md` for details.
