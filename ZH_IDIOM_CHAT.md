# ZH_IDIOM_CHAT
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://www.chineseidioms.com/
SOURCE_STATE: rule_only

USE_WHEN:
- 成语谚语 row needs a natural Chinese idiom-like full message

ALLOW_WHEN_NATURAL:
- 稳扎稳打: pacing, careful progress, project or negotiation rhythm
- 点到为止: gentle boundary, not over-explaining
- 留有余地: keep space, do not push too hard
- 见好就收: stop before overdoing, especially social pacing
- 欲速则不达: do not rush when speed may hurt result
- 顺水推舟: follow an already natural opening

BLOCK_WHEN:
- pure time/place/money/logistics
- factual translation only
- idiom makes the user sound old-fashioned or performative

OUTPUT_LOCK:
- never output only the idiom
- write the same meaning as a full chat sentence
- max one idiom

FINAL_SCAN:
- if it sounds like a slogan, output 无 / 无可用语
