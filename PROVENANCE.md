# Data provenance and rights context

This file documents the origin and rights context of materials included
in release v1.0.1. It does not attempt to relicense third-party content.

## CC0 dedication and scope

To the extent that the author holds copyright, database rights,
or related rights in the original research data, code, documentation,
annotations, scoring decisions, statistical outputs, and other original
materials in this release, those rights are dedicated to the public
domain under **CC0 1.0 Universal**.

This dedication applies only to rights that the author is legally able
to waive or license. It does not override rights in third-party or
pre-existing content.

In particular:

- Wikidata-derived structured data retains its original source provenance;
- Wikipedia-derived content remains subject to applicable Wikimedia
  terms where those rights apply;
- model-generated `response_text` may contain third-party or pre-existing
  material over which this release asserts no additional rights;
- public Wikimedia contributor identifiers remain subject to any
  applicable independent rights or privacy interests.

## Wikimedia sources

The research uses structured data from Wikidata and analytical data
derived from Kazakh Wikipedia.

The Kazakh Wikipedia dump files used to construct the analytical corpus
were retrieved from Wikimedia's `latest` dump endpoints on
**23 August 2026**. This is reported as a retrieval date rather than
as an independently verified internal Wikimedia snapshot date.

The release does not redistribute a complete Kazakh Wikipedia article
text dump. Its Wikipedia research files primarily contain identifiers,
page-level measurements, classifications, counts, and derived statistics.

## Wikidata-derived research tables

Files derived in whole or in part from Wikidata structured data include:

- `kazakhstan_territorial_universe.csv`
- `kkwiki_p31.csv`
- `p31_labels_verified.csv`
- `kazakhstan_p31_universe_final_detail.csv`
- `kazakhstan_p31_universe_final_summary.csv`
- `kazakhstan_p31_class_coverage_exploded.csv`
- `kazakhstan_external_gap_p31_master.csv`
- `kazakhstan_human_gender_corrected.csv`
- `kazakhstan_human_gender_corrected_summary.csv`
- `kazakhstan_human_gender_final.csv`

## Kazakh Wikipedia analytical tables

Files containing derived analytical measurements and summaries include:

- `kkwiki_analytical_corpus.csv`
- `kkwiki_thematic_depth.csv`
- `kkwiki_standardization_by_p31.csv`
- `kkwiki_creator_summary.csv`
- `kazakhstan_gender_depth.csv`
- `gender_depth_continuous_tests.csv`
- `gender_depth_categorical_tests.csv`

`kkwiki_creator_summary.csv` contains public Wikimedia contributor
identifiers used for creator-concentration analysis.

The publication-safety audit of release v1.0.1 detected no email addresses
and no credential-like strings.

## AI benchmark material

The AI benchmark contains frozen prompts, model responses, human
scoring/adjudication fields, and derived statistical results.

The evaluated models are:

- GPT-5.6 Terra
- Gemini 3.6 Flash

Primary row-level scoring files are:

- `ai_benchmark_recognition_scoring_FINAL_UNBLINDED_v1.1.csv`
- `ai_benchmark_factual_scoring_FINAL_UNBLINDED_v1.0.csv`

These files preserve frozen model outputs so that scoring decisions and
statistical analyses can be independently inspected without making new
requests to model providers.

The `response_text` fields contain model-generated material. The CC0
dedication for this release does not assert additional rights over
third-party or pre-existing material that may occur within such outputs.

Human-created scoring, adjudication, code, documentation, and analytical
work are distinct from the model-generated response text.

## Reproducibility

The main reproduction entry point is:

- `analysis_reproduction.ipynb`

The notebook reproduces the principal frozen Wikipedia/Wikidata, gender,
and AI benchmark results from the released data files.

## Release integrity

SHA-256 hashes are recorded in `manifest_release_v1.0.1.json`.
The manifest is regenerated only after all publication files and
metadata are finalized.
