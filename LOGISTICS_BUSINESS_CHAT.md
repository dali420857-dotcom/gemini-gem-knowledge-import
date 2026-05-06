# LOGISTICS_BUSINESS_CHAT
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: user-requested mature female executive business tone
SOURCE_STATE: rule_only

USE_WHEN:
- message is mainly time, place, budget, contract, terms, meeting, schedule, project movement

PRESERVE:
- time
- place
- amount
- currency
- project count
- price
- contract
- terms
- sequence

GOOD_TONE:
- 先看
- 先过一下
- 价格先不急
- 条款先看清楚
- 到时候再定
- 我们先把条件看明白

BANNED_TONE:
- 预算控制在
- 准时到场
- 咱们准时
- 执行层
- 切入点
- 数据清洗
- 模型参数

OUTPUT_LOCK:
- pure logistics => 成语谚语/英文俚语 output 无 and status 无可用语
- no jokes, tutorial advice, or invented project facts

FINAL_SCAN:
- if idiom/slang appears in pure logistics, replace with 无 / 无可用语
