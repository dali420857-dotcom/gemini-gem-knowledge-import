# AGREE_SHAPE_SOURCES
STATUS: source_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: GitHub-first sources for agree-shape, reflective listening, and non-sycophantic response rules

USE_WHEN:
- maintaining AGREE_SHAPE_PATTERNS.md
- checking whether "acknowledge without agreeing" has education or dialogue-system support

GH_SOURCES:
- anuradha1992/Motivational-Interviewing-Dataset => https://github.com/anuradha1992/Motivational-Interviewing-Dataset => USE_FOR: listener utterances annotated from MITI-derived labels; supports reflection/listening strategy research => SOURCE_STATE: research_dataset_cc_by_nc_sa => IMPORT_MODE: source_index_only
- IzzetYoung/CAMI => https://github.com/IzzetYoung/CAMI => USE_FOR: counselor agent using motivational interviewing strategy selection and response ranking => SOURCE_STATE: research_code_reference => IMPORT_MODE: source_index_only
- Sahandfer/EMPaper => https://github.com/Sahandfer/EMPaper => USE_FOR: paper index for empathy, emotion, reflective listening, emotional support dialogue => SOURCE_STATE: bibliography_index => IMPORT_MODE: source_index_only

LOWER_PRIORITY_GH:
- communication-skills gists can contain useful summaries but are personal notes, not primary sources
- do not import gist content as verified education rule unless backed by stronger source

NON_GH_BACKUP:
- NCBI active listening
- VA active listening for mediators
- university communication/assertiveness handouts
- Psychology Tools I-statements

SOURCE_BOUNDARY:
- these sources support concepts, not direct copy-paste rules
- no counseling dataset content should be imported into Gem
- keep AGREE_SHAPE_PATTERNS.md as rule_only, backed by this source index

FINAL_SCAN:
- prefer GH research repos first
- use non-GH education pages only when GH source is too broad or not directly explanatory
