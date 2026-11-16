# Release QA report - v1.0 (2026-11-15)

## Content scan (all CSV/XLSX/text files)
- Restricted columns (abstract, keywords, *_quote, pdf_location, link): none found.
- Cells longer than 600 characters: 3, all of them search strings (`01_search/search_strings.csv`, `01_search/openalex_supplementary_query.csv`, sheet S3 of the public workbook). This is expected.
- E-mail addresses: none. Local paths, Drive links or retrieval-folder references: none.

## Count and join checks
- PASS Included reports = 151
- PASS Included = coder-1 FT_eligible yes
- PASS Included origin split 92 / 59
- PASS Coder-1 rows 173; excluded 22
- PASS Excluded-22 source_ids = coder-1 "no" via key
- PASS Coder-2 rows 30 = key in_coder2_sample
- PASS Key CAN ids = 110 provenance ids
- PASS 110 provenance ids all in 3,839 ledger
- PASS Key SUP ids = 63 new includes
- PASS Ledger rows 3,839 unique
- PASS Human TA 142: 76 Include / 37 Unclear / 29 Exclude
- PASS Retrieval table 113 rows
- PASS LLM pre-screen: 3,223 screened + 100 filter check
- PASS LLM Include+Unclear among screened = 142
- Eligibility agreement recomputed from the coder files: Cohen's kappa = 0.714, PABAK = 0.867 (manuscript: 0.71 / 0.87).

## Known gaps in v1.0
1. `01_search/database_records_identifiers.csv` holds 10,751 records. Scopus search set A (`SCOPUS_A_v1_2026-09-17_raw.csv`, 11.6 MB) is not yet included because it exceeded the 10 MB transfer limit. Until it is added, the total cannot be reconciled with the 14,274 records exported.
2. Record-level title/abstract decisions of the database arm (11,657 records) were not available to this release. Only the counts are given.
3. The mapping of export-file search sets (Scopus A/B1/B2, IEEE A/B1/B2, SpringerLink 01-06, ScienceDirect 01-06) to search tracks A-D2 needs confirmation by the authors. The ScienceDirect exports present are from a folder labelled supplemental.
4. `IEEE_A_v1_p22_2101-2162.bib` contains 63 entries against a range label of 62.
