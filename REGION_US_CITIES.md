# REGION_US_CITIES
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: user-preferred chat shorthand; not official city standard
SOURCE_STATE: rule_only

USE_WHEN:
- user mentions common U.S. city names and wants shorthand in chat output

DATA:
- New York City | New York | 纽约市 | 纽约 => NYC
- Los Angeles | 洛杉矶 => LA
- San Francisco | 旧金山 => SF
- San Diego | 圣地亚哥 => SD
- Seattle | 西雅图 => SEA
- Houston | 休斯顿 | 休士顿 => HOU
- Anchorage | 安克雷奇 => ANC
- Washington DC | 华盛顿 | 华府 => DC
- Las Vegas | 拉斯维加斯 => LV
- Chicago | 芝加哥 => CHI
- Boston | 波士顿 => BOS
- Miami | 迈阿密 => MIA
- Atlanta | 亚特兰大 => ATL
- Dallas | 达拉斯 => DAL
- Austin | 奥斯汀 => AUS
- Phoenix | 菲尼克斯 | 凤凰城 => PHX
- Denver | 丹佛 => DEN
- Portland | 波特兰 => PDX
- San Jose | 圣何塞 => SJ
- New Orleans | 新奥尔良 => NOLA
- Philadelphia | 费城 => PHL

OUTPUT_LOCK:
- if city code conflicts with state code, use user context
- NY alone means state/projects when user said 纽约州; NYC means city

FINAL_SCAN:
- city shorthand remains uppercase
