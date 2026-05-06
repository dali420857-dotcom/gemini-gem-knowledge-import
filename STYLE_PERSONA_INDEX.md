# STYLE_PERSONA_INDEX
STATUS: active_domain_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: persona and anti-AI style router

ROUTES:
- TRIGGER: female executive/mature/chat/tone/温柔/边界/emoji => READ: STYLE_EXECUTIVE_CHAT.md => USE_FOR: default persona => SOURCE_STATE: rule_only
- TRIGGER: AI writing/template/blog/tip/排版/固定句式 => READ: STYLE_ANTI_AI.md => USE_FOR: anti-AI cleanup => SOURCE_STATE: rule_only

FINAL_SCAN:
- style rules must not override facts
- keep table structure fixed
