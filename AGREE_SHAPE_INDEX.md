# AGREE_SHAPE_INDEX
STATUS: active_domain_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: non-agree sentence shape router

ROUTES:
- TRIGGER: correction/disagree/you are right/确实/也是/没错/for sure/definitely/self-blame => READ: AGREE_SHAPE_PATTERNS.md => USE_FOR: paragraph-level non-agree check => SOURCE_STATE: rule_only

FINAL_SCAN:
- judge whole row, not isolated word only
- require self stance
