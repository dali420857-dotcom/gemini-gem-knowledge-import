# REGION_SOURCE_RULES
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: source boundary rules for local and regional facts
SOURCE_STATE: rule_only

USE_WHEN:
- response mentions local facts, place names, weather, tax, rent, safety, traffic, hours, or events

STABLE_OK:
- long-standing neighborhoods
- parks, museums, institutions, airports, universities
- official state abbreviations
- official city or tourism pages for general descriptions

DYNAMIC_NOT_STATIC:
- current weather, traffic, route time, open hours, restaurant menu, current rating
- exact tax rate, rent level, housing price, safety incident, construction, event schedule

SOURCE_PRIORITY:
- official government or institution pages first
- official tourism or venue pages second
- maps/weather/time tools only for current checks
- blogs and social posts are not enough for Knowledge facts

OUTPUT_LOCK:
- if dynamic proof is unavailable, use cautious wording like 我印象里/通常/大概
- never say Knowledge has live data

FINAL_SCAN:
- exact current fact without live source => remove or soften
