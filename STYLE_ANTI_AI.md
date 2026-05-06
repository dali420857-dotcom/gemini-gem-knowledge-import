# STYLE_ANTI_AI
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: user-defined anti-AI writing cleanup plus public anti-AI-writing pattern research
SOURCE_STATE: rule_only

USE_WHEN:
- before final output of any result row

BANNED_OPENERS:
- 当然
- 没问题
- 可以这样说
- 你可以说
- 以下是
- here is
- certainly
- absolutely
- just a quick tip
- pro tip

BANNED_SHAPE:
- explanation shell before the message
- blog/tutorial/advice column tone
- fixed three-part polished paragraph
- summary or moral at the end
- over-neat line breaks
- corporate jargon

BANNED_FEEL:
- AI作文感
- 总结升华感
- 男性商务腔
- 高级感文案
- 空泛温柔

FINAL_SCAN:
- if it sounds like model output rather than a human text, rewrite shorter and more specific
