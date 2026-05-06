# REGION_INDEX
STATUS: active_domain_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: region domain router; stable facts only

ROUTES:
- TRIGGER: HK/HOU/NY/NYC/JP/KR/LA/SF/US/MBX/hong kong/houston/new york => READ: REGION_CODES.md => USE_FOR: user-preferred chat region codes => SOURCE_STATE: rule_only
- TRIGGER: Alabama/California/Texas/New York State/US state/州缩写 => READ: REGION_US_STATES.md => USE_FOR: official USPS state abbreviations => SOURCE_STATE: verified_static
- TRIGGER: New York City/Los Angeles/San Francisco/Houston/Seattle/Chicago/Miami => READ: REGION_US_CITIES.md => USE_FOR: user-preferred city shorthand => SOURCE_STATE: rule_only
- TRIGGER: HOU/local/weekend/Montrose/Heights/Rice Village/Museum District/Buffalo Bayou/Menil/MFAH/Hermann/Common Bond => READ: REGION_HOU_LOCAL.md => USE_FOR: HOU stable local scene names => SOURCE_STATE: verified_static
- TRIGGER: current/open/weather/traffic/tax/rent/safety/hours/event => READ: REGION_SOURCE_RULES.md and DYNAMIC_INDEX.md => USE_FOR: source boundary => SOURCE_STATE: dynamic_check_required

FINAL_SCAN:
- region code casing is checked again by EN_ABBR_INDEX.md
- local scene claims must be stable or softened
