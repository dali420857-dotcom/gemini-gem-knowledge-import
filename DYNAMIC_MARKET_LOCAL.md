# DYNAMIC_MARKET_LOCAL
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: dynamic local facts boundary
SOURCE_STATE: dynamic_check_required

USE_WHEN:
- user asks tax, rent, house price, cost of living, safety, construction, medical access, local policy

RULES:
- these facts change by date and source
- use official city/state/county pages for tax and policy
- use current reputable data only when live search is available
- use cautious general wording when no live source exists

OUTPUT_LOCK:
- no exact tax/rent/safety/construction claim from static Knowledge
- do not make legal, medical, or financial advice

FINAL_SCAN:
- exact current number or risk claim without source => remove or soften
