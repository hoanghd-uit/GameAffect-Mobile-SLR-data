# Data and coding materials for: From Sensing to Anticipation on the Phone: A PRISMA 2020 Systematic Review of Player-Affect Modelling in Mobile Games

Release **v1.0** (2026-11-15). Authors: Ha Dang Hoang and Do Trong Hop, University of Information Technology, Vietnam National University, Ho Chi Minh City, Vietnam.

This repository holds the search records, screening decisions, coding forms, codebook, agreement analyses and the list of the **151 included reports** with their codes for the review named above (IEEE Transactions on Affective Computing, under review). Cite the archived version by its DOI (see `CITATION.cff`).

## Corpus at a glance

| Stage | n |
|---|---|
| Database arm: records exported (Scopus, IEEE Xplore, ScienceDirect, SpringerLink; 19 Sep 2026) | 14,274 |
| Database arm: reports sought / mobile-core reports carried forward | 3,839 / 110 |
| Supplementary arm (OpenAlex, 11 Nov 2026): records identified / LLM pre-screened / human title-abstract screened | 14,802 / 3,223 / 142 |
| Supplementary arm: sought / assessed in full / eligible | 101 / 66 / 63 |
| Candidates coded from full text by a human (110 + 63) | 173 |
| Excluded at full-text coding (18 original + 4 supplementary) | 22 |
| **Included reports (92 original + 59 supplementary)** | **151** |
| Double-coded by a second human coder | 30 |

## Layout and mapping to the paper

- `01_search/` - Search (Section 3.2 and Appendix A; supplementary Table S3)
- `02_screening/` - Study selection (Sections 3.3 and 4.1; PRISMA flow figure)
- `03_coding/` - Full-text human coding (Section 3.5; supplementary Table S2)
- `04_agreement/` - Coding reliability (Section 4.2; coding-agreement table; supplementary Tables S5-S6)
- `05_included/` - Included corpus and synthesis (Sections 5-6; supplementary Tables S1, S4, S7-S10)
- `06_llm/` - LLM assistance (Section 3.4; Use of Generative AI statement)
- `supplementary/` - Journal supplementary workbook

| File | Rows | Content |
|---|---|---|
| `01_search/search_strings.csv` | 21 | Search strings per track and platform (Scopus and OpenAlex verbatim; IEEE/ScienceDirect/SpringerLink reconstructed) |
| `01_search/database_records_identifiers.csv` | 10751 | Identifier-only list of database-search records as exported (no abstracts, authors or keywords); Scopus search set A pending |
| `01_search/openalex_supplementary_query.csv` | 11 | OpenAlex supplementary query as run on 2026-11-11 |
| `01_search/openalex_supplementary_flow_counts.csv` | 16 | Record flow of the OpenAlex supplementary search |
| `02_screening/database_arm/prisma_counts_v19.csv` | 22 | PRISMA counts of the database arm (v19 freeze, broad game-affect review) |
| `02_screening/database_arm/fulltext_eligibility_ledger_3839.csv` | 3839 | Eligibility ledger of the 3,839 reports sought in the database arm (broad game-affect review) |
| `02_screening/database_arm/mobile_core_110_provenance.csv` | 110 | The 110 mobile-core reports carried from the database arm, with the evidence source used by the original pipeline |
| `02_screening/supplementary_arm/llm_prescreen_decisions_3323.csv` | 3323 | LLM title/abstract pre-screen decisions: 3,223 screened records plus 100-record noise-filter check (stratum filtered_out_sample100) |
| `02_screening/supplementary_arm/human_title_abstract_screening_142.csv` | 142 | Human title/abstract screening of the 142 LLM Include/Unclear candidates (human reasons partly in Vietnamese) |
| `02_screening/supplementary_arm/retrieval_and_fulltext_113.csv` | 113 | 113 records kept at title/abstract: second-look removals, retrieval status, full-text decision |
| `02_screening/supplementary_arm/removed_before_retrieval_12.csv` | 12 | Removed before retrieval with reasons |
| `02_screening/supplementary_arm/not_retrieved_35.csv` | 35 | Reports sought but not retrieved, with reasons |
| `02_screening/supplementary_arm/not_retrieved_reasons_summary.csv` | 6 | Counts of not-retrieved reasons |
| `02_screening/supplementary_arm/fulltext_excluded_3.csv` | 3 | Excluded at full-text eligibility |
| `02_screening/supplementary_arm/new_includes_63.csv` | 63 | 63 supplementary reports eligible at full text (entered human coding) |
| `02_screening/supplementary_arm/pdf_identity_qa_67.csv` | 67 | PDF identity check of retrieved full texts |
| `02_screening/supplementary_arm/prisma_counts_supplementary.csv` | 20 | PRISMA counts of the supplementary arm |
| `03_coding/codebook_59_variables.csv` | 59 | Codebook used for human full-text coding (59 variables) |
| `03_coding/codebook_allowed_values.csv` | 10 | Allowed values per coded variable (drop-down lists of the coding form) |
| `03_coding/coder1_fulltext_coding_173.csv` | 173 | Coder 1 (first author) full-text codes for all 173 candidates, as entered |
| `03_coding/coder2_fulltext_coding_30.csv` | 30 | Coder 2 independent full-text codes for the 30-report sample, as entered |
| `03_coding/coder1_model_details.csv` | 10 | Coder 1 details of trained affect models |
| `03_coding/coder1_adaptation_details.csv` | 3 | Coder 1 details of affect-driven adaptation studies |
| `03_coding/coder2_model_details.csv` | 9 | Coder 2 details of trained affect models |
| `03_coding/coder2_adaptation_details.csv` | 2 | Coder 2 details of affect-driven adaptation studies |
| `03_coding/report_id_key.csv` | 173 | Key from neutral report_id (R###) to source_id (CAN = database arm, SUP = supplementary arm) and coder-2 sample flag |
| `03_coding/llm_codes_original_110.csv` | 110 | LLM-pipeline codes for the 110 original reports (used only for the human-vs-LLM comparison; verbatim quote columns removed) |
| `03_coding/coding_form_template.xlsx` | 173 | Blank coding form (identifiers and titles only) with codebook and drop-down lists |
| `04_agreement/human_vs_human_30.csv` | 49 | Human-human agreement (30 reports; 25 both eligible): raw, Cohen kappa, PABAK |
| `04_agreement/human_vs_llm_110.csv` | 43 | Human vs LLM agreement on the 110 original reports |
| `04_agreement/human_vs_llm_by_evidence_source.csv` | 27 | Human vs LLM agreement stratified by the evidence the LLM used (full text / abstract / title) |
| `04_agreement/llm_lane_intercoder_agreement.csv` | 28 | Agreement between the two LLM coding lanes of the original pipeline |
| `05_included/included_reports_151.csv` | 151 | 151 included reports with all coder-1 codes, research stream and maturity level |
| `05_included/excluded_at_coding_22.csv` | 22 | 22 reports excluded at full-text coding, with reasons |
| `05_included/pillar_counts.csv` | 45 | Pillar counts with Wilson 95% CI, by origin |
| `05_included/model_details_10.csv` | 10 | Trained-model details (10 reports) |
| `05_included/adaptation_details_3.csv` | 3 | Adaptation-study details (3 reports) |
| `05_included/maal_application_12.csv` | 12 | MAAL stage application to 12 model/adaptation reports |
| `05_included/taxonomy.csv` | 48 | Taxonomy layers, dimensions, categories with report counts |
| `06_llm/supplementary_prescreen_prompt.json` | 1 | Frozen system prompt and criteria for the LLM pre-screen of the supplementary arm |
| `supplementary/Supplementary_Material_S1-S10_public.xlsx` | 12 | Journal supplementary workbook S1-S10 with abstracts and file paths removed |

## Identifiers and joins

- `report_id` (R001-R173) is the neutral identifier shown to coders. `03_coding/report_id_key.csv` maps it to `source_id`.
- `source_id` / `canonical_id`: `CAN#####` = report from the database arm (same IDs as the broad game-affect review ledger); `SUP###` = report from the supplementary OpenAlex arm (`sup_id`).
- `openalex_id` links supplementary-arm records across the LLM pre-screen, human screening and retrieval tables.
- `doi` is lower-case without the `https://doi.org/` prefix where it was normalised.

## Conventions

- Coder files (`03_coding/coder*_fulltext_coding_*.csv`) are **as entered**. Model-dependent variables (`player_level_model`, `subject_independent`, `leakage_control`) are blank when no affect model was trained. In `05_included/included_reports_151.csv` and the S1 sheet those blanks are written as `no` (141 of 151 rows).
- `session_design` had low human-human agreement (raw 0.28) and is reported descriptively only.
- Human title/abstract reasons in `human_title_abstract_screening_142.csv` and `retrieval_and_fulltext_113.csv` are partly written in Vietnamese.
- In `01_search/search_strings.csv` the Scopus and OpenAlex strings are verbatim. The IEEE Xplore, ScienceDirect and SpringerLink strings are reconstructed adaptations, because the strings actually run were not archived.
- `01_search/database_records_identifiers.csv` lists the records as exported, before de-duplication. `search_set` is the label of the export file. One IEEE export file (`IEEE_A_v1_p22_2101-2162.bib`) contains 63 entries against a range label of 62.
- The database-arm tables in `02_screening/database_arm/` are shared with the companion broad review of affective computing in digital games (614 included reports). Only the 110 `MOBILE_CORE` reports enter this review.

## What is not included, and why

- **Abstracts, author keywords, author lists and verbatim quotations** from the indexed reports are excluded. They are third-party content licensed by the database providers and publishers. Titles, DOIs, years and venues are kept as bibliographic facts.
- **Full-text PDFs** are not redistributed.
- **Raw database export files** are not redistributed. Their identifiers are in `01_search/database_records_identifiers.csv`.
- **Record-level title/abstract decisions of the database arm (11,657 records)** are not part of v1.0. Their counts are in `02_screening/database_arm/prisma_counts_v19.csv`.

## Use of generative AI

Claude-family large language models (Anthropic) assisted the original database review in screening and first-pass extraction. Claude Sonnet 5 pre-screened supplementary OpenAlex records under the frozen prompt in `06_llm/`. Every one of the 173 candidates was re-assessed and coded from full text by a human, and no automated decision enters the final corpus. LLM outputs are released only to document the pre-screen and the human-vs-LLM comparison.

## Licence

Data and documentation: Creative Commons Attribution 4.0 International (CC BY 4.0), see `LICENSE`. Bibliographic metadata of third-party reports (titles, DOIs, venues) are factual records and are included for identification only.

## Integrity

`MANIFEST.sha256` lists a SHA-256 checksum for every file. `QA_report.md` records the release checks.
