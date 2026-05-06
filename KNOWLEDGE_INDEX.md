# KNOWLEDGE_INDEX
STATUS: active_top_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: domain router for Gemini Gem Knowledge; keep short and route only

ROUTES:
- TRIGGER: region/place/city/state/local/HK/HOU/NY/NYC => READ: REGION_INDEX.md => USE_FOR: region codes and local static facts => SOURCE_STATE: mixed_index
- TRIGGER: current/weather/time/map/open/traffic/tax/rent/safety/construction => READ: DYNAMIC_INDEX.md => USE_FOR: live-check gate => SOURCE_STATE: dynamic_check_required
- TRIGGER: news/current affairs/finance/investment/stock/market/SEC/FRED/AI trend/latest repo/latest paper => READ: DYNAMIC_INDEX.md => USE_FOR: live news, finance, stock, and AI source gate => SOURCE_STATE: dynamic_check_required
- TRIGGER: chengyu/proverb/谚语/成语/俗语 => READ: ZH_LITERATURE_INDEX.md => USE_FOR: Chinese literary expression => SOURCE_STATE: rule_only
- TRIGGER: idiom/slang/proverb/俚语 => READ: EN_LITERATURE_INDEX.md => USE_FOR: English expression => SOURCE_STATE: rule_only
- TRIGGER: abbreviation/casing/lowercase/uppercase/HK/HOU/NY/NYC => READ: EN_ABBR_INDEX.md => USE_FOR: abbreviation and casing final scan => SOURCE_STATE: rule_only
- TRIGGER: logistics/contract/budget/meeting/project/schedule/terms => READ: LOGISTICS_INDEX.md => USE_FOR: factual business rewrite => SOURCE_STATE: rule_only
- TRIGGER: agree/correction/disagree/self-blame/you are right/确实/也是 => READ: AGREE_SHAPE_INDEX.md => USE_FOR: non-agree sentence shape => SOURCE_STATE: rule_only
- TRIGGER: tone/style/emoji/AI writing/female executive => READ: STYLE_PERSONA_INDEX.md => USE_FOR: persona and anti-AI style => SOURCE_STATE: rule_only
- TRIGGER: public GitHub knowledge/open knowledge base/source repo/external KB => READ: PUBLIC_GH_KB_INDEX.md => USE_FOR: source selection and import boundary => SOURCE_STATE: source_index

READ_ORDER:
- read the most specific matching domain only
- if multiple domains match, read at most 3 domain indexes
- never read all files

FINAL_SCAN:
- route before answering
- avoid unrelated domains to reduce thinking time
