# REGION_US_STATES
STATUS: active_topic
SOURCE_DATE: 2026-05-06
SOURCE_URL: https://about.usps.com/who/profile/history/state-abbreviations.htm
SOURCE_STATE: verified_static

USE_WHEN:
- user mentions a U.S. state name or Chinese state name

DATA:
- Alabama => AL
- Alaska => AK
- Arizona => AZ
- Arkansas => AR
- California | 加州 => CA
- Colorado => CO
- Connecticut => CT
- Delaware => DE
- Florida | 佛州 => FL
- Georgia => GA
- Hawaii => HI
- Idaho => ID
- Illinois => IL
- Indiana => IN
- Iowa => IA
- Kansas => KS
- Kentucky => KY
- Louisiana | 路易斯安那州 => LA
- Maine => ME
- Maryland => MD
- Massachusetts => MA
- Michigan => MI
- Minnesota => MN
- Mississippi => MS
- Missouri => MO
- Montana => MT
- Nebraska => NE
- Nevada => NV
- New Hampshire => NH
- New Jersey => NJ
- New Mexico => NM
- New York State | 纽约州 => NY
- North Carolina => NC
- North Dakota => ND
- Ohio => OH
- Oklahoma => OK
- Oregon => OR
- Pennsylvania => PA
- Rhode Island => RI
- South Carolina => SC
- South Dakota => SD
- Tennessee => TN
- Texas | 德州 | 得州 => TX
- Utah => UT
- Vermont => VT
- Virginia => VA
- Washington State | 华盛顿州 => WA
- West Virginia => WV
- Wisconsin => WI
- Wyoming => WY
- Washington DC | 华盛顿特区 | 华府 => DC

FINAL_SCAN:
- USPS state abbreviations stay uppercase
- state names in Chinese output may use code when user expects shorthand
