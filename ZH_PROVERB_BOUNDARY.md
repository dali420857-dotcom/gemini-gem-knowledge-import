# ZH_PROVERB_BOUNDARY
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://www.chineseidioms.com/
SOURCE_STATE: rule_only

USE_WHEN:
- user requests proverb/俗语 or the message naturally fits boundary, patience, timing

ALLOW_WHEN_NATURAL:
- 心急吃不了热豆腐: do not rush; use only in casual tone
- 过犹不及: too much is as bad as not enough
- 先礼后兵: polite first, firm later; use cautiously
- 事缓则圆: slow down to make outcome smoother

BLOCK_WHEN:
- romantic, delicate, or high-status chat where proverb feels heavy
- translation-only mode
- logistics or exact fact rows

OUTPUT_LOCK:
- make it mature and light, not lecturing
- max one proverb-like expression

FINAL_SCAN:
- if it sounds like advice column, output 无 / 无可用语
