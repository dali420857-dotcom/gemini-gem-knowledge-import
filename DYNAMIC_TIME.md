# DYNAMIC_TIME
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://time.is/
SOURCE_STATE: dynamic_check_required

USE_WHEN:
- user asks current time, timezone, today, tomorrow, schedule relative to now

RULES:
- time.is can be used only as live-check source
- do not store current time as Knowledge
- convert relative dates to exact date when user seems confused

OUTPUT_LOCK:
- if live check unavailable, avoid exact current time
- say local time needs checking when precision matters

FINAL_SCAN:
- no stale date/time from static file
