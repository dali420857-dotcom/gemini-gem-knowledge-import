# DYNAMIC_MAPS
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://www.google.com/maps
SOURCE_STATE: dynamic_check_required

USE_WHEN:
- user asks route, traffic, open hours, nearby places, current place status, map details

RULES:
- Google Maps can live-check existence, route, hours, nearby context
- do not import full map database into Knowledge
- venue existence can be static only when also backed by official venue page

OUTPUT_LOCK:
- if live map check unavailable, avoid open now, busy, exact drive time
- use stable place names or neighborhood direction

FINAL_SCAN:
- current route/hours/nearby claim without live source => soften or remove
