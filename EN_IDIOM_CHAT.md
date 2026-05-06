# EN_IDIOM_CHAT
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://dictionary.cambridge.org/us/dictionary/english/play-it-safe ; https://dictionaryblog.cambridge.org/2019/08/07/the-balls-in-your-court-now-idioms-with-ball/
SOURCE_STATE: rule_only

USE_WHEN:
- English idiom row needs a natural complete message

ALLOW_WHEN_NATURAL:
- play it safe: cautious choice, risk control
- get the ball rolling: start gently
- keep an eye on it: monitor without rushing
- on the same page: aligned understanding

BLOCK_WHEN:
- pure logistics, exact money/time/contract
- idiom makes message too corporate
- translation-only mode

OUTPUT_LOCK:
- same facts and posture as English row
- max one idiom
- lowercase except region codes

FINAL_SCAN:
- if idiom sounds like business jargon, output 无 / 无可用语
