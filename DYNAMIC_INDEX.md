# DYNAMIC_INDEX
STATUS: active_domain_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: dynamic facts are gates, not static truth

ROUTES:
- TRIGGER: now/current/time/timezone/date/today/tomorrow => READ: DYNAMIC_TIME.md => USE_FOR: time gate => SOURCE_STATE: dynamic_check_required
- TRIGGER: weather/wind/rain/storm/temperature/forecast/air quality => READ: DYNAMIC_WEATHER.md => USE_FOR: weather gate => SOURCE_STATE: dynamic_check_required
- TRIGGER: map/route/traffic/open/hours/nearby/place exists => READ: DYNAMIC_MAPS.md => USE_FOR: map gate => SOURCE_STATE: dynamic_check_required
- TRIGGER: tax/rent/price/safety/construction/medical/current local cost => READ: DYNAMIC_MARKET_LOCAL.md => USE_FOR: local market gate => SOURCE_STATE: dynamic_check_required

FINAL_SCAN:
- dynamic facts require live source or cautious wording
- static Knowledge cannot prove current status
