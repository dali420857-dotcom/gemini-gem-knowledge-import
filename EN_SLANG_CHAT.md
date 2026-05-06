# EN_SLANG_CHAT
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://dictionary.cambridge.org/
SOURCE_STATE: rule_only

USE_WHEN:
- English slang row or +slang/+俚语 asks for a light natural phrase

ALLOW_WHEN_NATURAL:
- no rush: relaxed pacing
- keep it low-key: discreet tone
- play it cool: calm social posture
- fair enough: soft acceptance without over-agreeing
- sounds good: simple agreement only when user wants agreement

BLOCKED_DEFAULT:
- just a quick tip
- pro tip
- touch base
- hit up
- on the dot
- dont jump the gun in logistics
- go with the flow in contracts

OUTPUT_LOCK:
- no slang if it weakens mature female executive tone
- no forced slang in serious money/legal/medical/logistics

FINAL_SCAN:
- if slang feels young, performative, or blog-like, output 无 / 无可用语
