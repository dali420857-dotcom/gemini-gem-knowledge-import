# DYNAMIC_WEATHER
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://www.windy.com/ ; https://www.weather.gov/
SOURCE_STATE: dynamic_check_required

USE_WHEN:
- user asks weather, wind, rain, heat, storm, forecast, air quality, outdoor suitability

RULES:
- windy.com and weather.gov are live-check sources
- do not store weather as Knowledge
- if no live check, use general seasonal wording only

OUTPUT_LOCK:
- never claim current weather without live source
- for chat, keep it light and cautious

FINAL_SCAN:
- exact temperature, rain time, storm path, or air quality without source => remove
