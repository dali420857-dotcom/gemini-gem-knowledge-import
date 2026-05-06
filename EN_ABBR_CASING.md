# EN_ABBR_CASING
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: user-requested casual English typing style
SOURCE_STATE: rule_only

USE_WHEN:
- producing English or English slang row

RULES:
- default English uses lowercase like casual phone/computer typing
- keep region codes uppercase
- do not auto-capitalize sentence start
- do not auto-capitalize standalone i
- do not force brand/person title casing unless user asks formal
- sentence-internal period is allowed
- final punctuation is removed

BLOCKED_PUNCTUATION:
- comma
- apostrophe
- quote
- semicolon
- colon
- question mark
- exclamation mark

FINAL_SCAN:
- delete final punctuation
- if punctuation cleanup makes sentence awkward, rewrite shorter
