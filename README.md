# Gemini Gem Knowledge
STATUS: active_public_import_set
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: import instructions for this Knowledge file set

ENTRY:
- start with KNOWLEDGE_INDEX.md
- read only the matching domain index
- read only the matching topic file
- do not read all files

DOMAINS:
- REGION: region shorthand, USPS state codes, HOU static local facts
- DYNAMIC: live-check gates for time, weather, maps, local market facts
- ZH_LITERATURE: Chinese idiom/proverb expression gates
- EN_LITERATURE: English idiom/slang expression gates
- EN_ABBR: English casing and region-code cleanup
- LOGISTICS: factual business/logistics rewrite gates
- AGREE_SHAPE: paragraph-level non-agree rules
- STYLE_PERSONA: mature female executive tone and anti-AI style
- PUBLIC_GH_KB: external GitHub knowledge source boundary

IMPORT_RULE:
- import these markdown files as Gem Knowledge
- keep each file under 100 lines where possible
- dynamic facts are not stored as static truth
- public GitHub repos are source references, not bulk imports

TEST_FIRST:
- verify KNOWLEDGE_INDEX routing
- verify at least one sentinel value
- measure output latency after import
