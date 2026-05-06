# REGION_HOU_LOCAL
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://www.houstontx.gov/superneighborhoods/24.html ; https://lgbtq.visithoustontexas.com/listings/common-bond/26738/ ; https://lgbtq.visithoustontexas.com/listings/hermann-park/22338/ ; https://www.menil.org/ ; https://www.mfah.org/ ; https://buffalobayou.org/location/buffalo-bayou-park/
SOURCE_STATE: verified_static

USE_WHEN:
- user asks HOU local life, weekend, where to go, resident-style scene

STABLE_NAMES:
- neighborhoods: montrose, the heights, rice village, museum district
- parks: buffalo bayou park, hermann park
- museums: menil collection, MFAH
- cafe: common bond on westheimer

CHAT_USE:
- use 1 or 2 stable names only
- sound like a local texting, not a travel guide
- pair a place with a simple activity: coffee, walk, museum, dinner nearby

DO_NOT_CLAIM_WITHOUT_LIVE_CHECK:
- open now, crowded now, menu today, exact price, current event, safety today, traffic now
- personal recent visit like yesterday/last week unless user said it

FINAL_SCAN:
- if claim is current/live, route to DYNAMIC_INDEX.md or soften
