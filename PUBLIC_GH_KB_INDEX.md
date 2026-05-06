# PUBLIC_GH_KB_INDEX
STATUS: source_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: public GitHub knowledge bases evaluated for Gemini Gem Knowledge

USE_WHEN:
- selecting external sources for future Knowledge updates
- deciding whether a public repo can be directly imported

VERDICT:
- do not import whole public repositories into Gem Knowledge
- import only short verified extracts or keep as source links
- whole repos increase noise, latency, licensing risk, and unrelated retrieval

APPROVED_SOURCE_INDEX:
- unicode-org/cldr => https://github.com/unicode-org/cldr => USE_FOR: locale, territory names, language data => SOURCE_STATE: verified_static_public_repo => IMPORT_MODE: source_link_or_extract
- dr5hn/countries-states-cities-database => https://github.com/dr5hn/countries-states-cities-database => USE_FOR: country/state/city reference when broad global list is needed => SOURCE_STATE: public_dataset_odbl => IMPORT_MODE: source_link_or_filtered_extract
- countries/countries => https://github.com/countries/countries => USE_FOR: ISO country objects, translations, currencies => SOURCE_STATE: public_dataset => IMPORT_MODE: source_link_or_filtered_extract
- country-regions/country-region-data => https://github.com/country-regions/country-region-data => USE_FOR: country/region short codes for address-like data => SOURCE_STATE: public_dataset => IMPORT_MODE: source_link_or_filtered_extract
- lyonzin/knowledge-rag => https://github.com/lyonzin/knowledge-rag => USE_FOR: markdown-aware chunking and local RAG architecture reference => SOURCE_STATE: architecture_reference => IMPORT_MODE: do_not_import_content
- dotenvx/llmstxt => https://github.com/dotenvx/llmstxt => USE_FOR: llms.txt generation pattern and source list architecture => SOURCE_STATE: architecture_reference => IMPORT_MODE: do_not_import_content
- anuradha1992/Motivational-Interviewing-Dataset => https://github.com/anuradha1992/Motivational-Interviewing-Dataset => USE_FOR: motivational interviewing listener labels and reflection research => SOURCE_STATE: research_dataset_cc_by_nc_sa => IMPORT_MODE: source_index_only
- IzzetYoung/CAMI => https://github.com/IzzetYoung/CAMI => USE_FOR: motivational interviewing counselor agent strategy architecture => SOURCE_STATE: research_code_reference => IMPORT_MODE: source_index_only
- Sahandfer/EMPaper => https://github.com/Sahandfer/EMPaper => USE_FOR: empathy and emotional support dialogue paper index => SOURCE_STATE: bibliography_index => IMPORT_MODE: source_index_only

NOT_DIRECT_IMPORT:
- large country/city datasets
- full CLDR repository
- full RAG tool repositories
- full llms.txt hubs
- any repo with unclear license or unverified crowd edits

DIRECT_IMPORT_ALLOWED_ONLY_IF:
- file is under 100 lines
- file has clear source and license
- file matches one domain only
- no dynamic facts are stored as static truth
- output latency remains within checklist thresholds

FINAL_SCAN:
- if a public GH repo is used, cite repo URL in the topic file
- never claim imported source is live-updating inside Gem unless Gem actually fetches latest file
