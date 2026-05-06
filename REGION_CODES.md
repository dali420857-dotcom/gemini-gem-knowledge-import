# REGION_CODES
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: user-preferred chat shorthand; not official postal/IATA truth except where stated

USE_WHEN:
- input or output has common regions, cities, or project locations

DATA:
- 香港 | hong kong => HK
- 休斯顿 | houston => HOU
- 纽约州 | new york state => NY
- 纽约市 | new york city => NYC
- 日本 | japan => JP
- 韩国 | korea => KR
- 洛杉矶 | los angeles => LA
- 旧金山 | san francisco => SF
- 美国 | united states | america => US
- 墨湾 | mobay => MBX TEST_ONLY sentinel, not real-world fact

OUTPUT_LOCK:
- these codes stay uppercase in Chinese and English rows
- do not change NY to NYC unless user says New York City/纽约市/NYC
- do not change HOU to Houston in output unless user requests full names

FINAL_SCAN:
- standalone hk/hou/ny/nyc/jp/kr/la/sf/us/mbx => uppercase
