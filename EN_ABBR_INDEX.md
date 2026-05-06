# EN_ABBR_INDEX
STATUS: active_domain_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: English abbreviation and casing router

ROUTES:
- TRIGGER: HK/HOU/NY/NYC/JP/KR/LA/SF/US/state/city => READ: EN_ABBR_REGION.md => USE_FOR: region code casing => SOURCE_STATE: rule_only
- TRIGGER: lowercase/uppercase/i/brand/name/final scan => READ: EN_ABBR_CASING.md => USE_FOR: English casing cleanup => SOURCE_STATE: rule_only

FINAL_SCAN:
- region codes uppercase
- casual English lowercase unless user asks formal
