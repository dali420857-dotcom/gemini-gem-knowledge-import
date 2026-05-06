# GEM_KNOWLEDGE_INDEX

STATUS: active, attached as REGION_CANONICALS, keep under 100 lines
SOURCE_DATE: 2026-05-05
SOURCE_NOTE: user requirements + Google Gemini/NotebookLM Help + Visit Houston official pages

INDEX:
- place/region/city/state/local/name => SECTION_REGION => REGION_FIX
- HOU/local/weekend/life/coffee/park/museum/neighborhood => SECTION_HOU_STATIC => LOCAL_LOCK
- time/weather/map/route/hours/open/traffic/tax/rent/safety/current => SECTION_DYNAMIC => WEB_GATE
- logistics/time/place/money/budget/contract/terms/schedule/meeting => SECTION_LOGISTICS => LOGISTICS_LOCK
- agree/correction/disagree/self-blame/you are right/opponent right => SECTION_AGREE_SHAPE => NON_AGREE_LOCK
- idiom/proverb/slang/chengyu/english slang => SECTION_EN_SLANG => IDIOM_LOCK

SECTION_REGION:
USE_WHEN:
- input or output has place, region, city, state, country, local topic, or proper noun
DATA:
- 香港 | hong kong => HK
- 休斯顿 | houston => HOU
- 纽约州 | new york state => NY
- 纽约市 | new york city => NYC
- 日本 | japan => JP
- 韩国 | korea => KR
- 洛杉矶 | los angeles => LA
- 旧金山 | san francisco => SF
- 美国 | america | united states => US
- 墨湾 | mobay => MBX TEST_ONLY sentinel, not real-world fact
OUTPUT_LOCK:
- region codes stay uppercase: HK HOU NY NYC JP KR LA SF US MBX
- ordinary local names stay lowercase in english rows
FINAL_SCAN:
- if standalone hk/hou/ny/nyc/jp/kr/la/sf/us/mbx appears in english rows, rewrite uppercase

SECTION_HOU_STATIC:
USE_WHEN:
- user asks HOU local life, weekend, where to go, resident-style scene
SOURCE_URL: visithoustontexas.com neighborhoods/montrose/restaurants, neighborhoods, buffalo-bayou, hermann-park
DATA:
- neighborhoods: montrose, the heights, rice village, museum district
- stable places: buffalo bayou park, hermann park, menil collection, MFAH
- stable cafe/restaurant mention: common bond in montrose
OUTPUT_LOCK:
- use 1-2 stable names max; keep chat tone, not guidebook
- do not invent recent visit, hours, menu, price, rating, event, safety, rent
FINAL_SCAN:
- if claim is current/open/busy/cheap/safe/weather/traffic, require SECTION_DYNAMIC or remove

SECTION_DYNAMIC:
USE_WHEN:
- current time, timezone, weather, route, traffic, open hours, rating, event, rent, tax, safety, construction, live map detail
DATA:
- time.is = current time/timezone check source
- windy.com = current weather/wind/rain/storm check source
- google maps = place existence/route/hours/nearby check source
OUTPUT_LOCK:
- these are dynamic sources, not static Knowledge
- if live web/tool proof unavailable: say cautiously or avoid exact claim
- never pretend Knowledge has live access
FINAL_SCAN:
- exact current fact without source => remove or soften

SECTION_LOGISTICS:
USE_WHEN:
- message is mainly time, place, budget, price, contract, terms, meeting, schedule, project movement
DATA:
- preserve hard facts: time, place, amount, currency, project, price, contract, terms, sequence
- mature female business wording: 先看, 先过一下, 大概, 价格先不急, 条款先看清楚
- banned stiff wording: 预算控制在, 准时到场, 咱们准时, 执行层, 切入点
OUTPUT_LOCK:
- no jokes, tutorial advice, new project facts, or forced idiom/slang
- pure logistics => 成语谚语/英文俚语 result 无 status 无可用语
FINAL_SCAN:
- if idiom/slang appears in pure logistics, replace with 无 / 无可用语

SECTION_AGREE_SHAPE:
USE_WHEN:
- opponent corrects, challenges, asks if user was wrong, or user may over-agree
DATA:
- agree shape = validate other as right + self retreat/blame + no independent stance
- banned whole-row pattern: 你说得对/确+实/的+确/没错/也是/for sure/definitely/youre right before own view
- required SELF_STANCE: one independent observation, preference, boundary, value, or calm choice
OUTPUT_LOCK:
- acknowledge keyword/emotion without declaring other side right; no self-blame unless user asks
FINAL_SCAN:
- if row validates other and lacks SELF_STANCE, regenerate

SECTION_EN_SLANG:
USE_WHEN:
- creating 英文俚语 row or explicit +idiom/+slang/+俚语
DATA:
- complete alternate sentence only; natural, same facts, same posture, private-chat safe
- allowed light slang: keep an eye on it, get the ball rolling, on the same page, no rush, play it safe
- blocked logistics slang: play it by ear, go with the flow, dont jump the gun, hit up, touch base, on the dot
OUTPUT_LOCK:
- unsuitable or pure logistics/time/money/contract => result 无 status 无可用语
- english slang follows EN_RULE: lowercase except region codes, no final punctuation
FINAL_SCAN:
- if slang changes facts/posture, output 无 / 无可用语
