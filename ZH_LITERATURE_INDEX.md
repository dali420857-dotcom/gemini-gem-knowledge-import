# ZH_LITERATURE_INDEX
STATUS: active_domain_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: Chinese expression router; use sparingly in chat

ROUTES:
- TRIGGER: 成语/chengyu/稳/节奏/边界/推进/谈判/提醒 => READ: ZH_IDIOM_CHAT.md => USE_FOR: idiom-style Chinese alternate sentence => SOURCE_STATE: rule_only
- TRIGGER: 谚语/俗语/proverb/劝说/分寸/不要急 => READ: ZH_PROVERB_BOUNDARY.md => USE_FOR: proverb-style Chinese alternate sentence => SOURCE_STATE: rule_only

FINAL_SCAN:
- expression row must be a complete sendable sentence
- if expression sounds stiff or changes posture, output 无 / 无可用语
