# EN_LITERATURE_INDEX
STATUS: active_domain_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: English idiom and slang router

ROUTES:
- TRIGGER: idiom/proverb/english idiom/boundary/pacing/project => READ: EN_IDIOM_CHAT.md => USE_FOR: natural English idiom row => SOURCE_STATE: rule_only
- TRIGGER: slang/casual phrase/俚语/texting => READ: EN_SLANG_CHAT.md => USE_FOR: light English slang row => SOURCE_STATE: rule_only

FINAL_SCAN:
- English expression must be a complete sendable sentence
- lowercase except region codes
- no final punctuation
