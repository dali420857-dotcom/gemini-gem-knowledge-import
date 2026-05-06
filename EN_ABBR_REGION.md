# EN_ABBR_REGION
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: final casing scan for region shorthand
SOURCE_STATE: rule_only

USE_WHEN:
- English output contains region or city shorthand

UPPERCASE_CODES:
- HK
- HOU
- NY
- NYC
- JP
- KR
- LA
- SF
- US
- TX
- CA
- WA
- DC
- MBX TEST_ONLY

RULES:
- standalone region code must be uppercase
- do not lowercase HOU inside English rows
- ordinary place names can stay lowercase in casual style

FINAL_SCAN:
- hk => HK
- hou => HOU
- ny => NY
- nyc => NYC
- jp => JP
- kr => KR
- mbx => MBX
