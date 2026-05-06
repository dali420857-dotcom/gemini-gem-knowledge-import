# DYNAMIC_NEWS_FINANCE_AI_SOURCES
STATUS: prepared_source_index
SOURCE_DATE: 2026-05-06
SOURCE_NOTE: GitHub metadata checked via GitHub REST API and GitHub page; official dynamic docs checked by web search

USE_WHEN:
- user asks current affairs/news/finance/investment/stocks/AI trend
- user asks latest, today, now, market, filing, macro, AI paper, AI repo, financial news

OUTPUT_LOCK:
- never store live news, prices, ratings, sentiment, or market levels as static Knowledge
- use this file to choose live source, then cite fresh source in the answer
- if live source is unavailable, say unable to verify current status and use cautious wording
- no investment advice; separate facts, source, time window, and uncertainty

OFFICIAL_DYNAMIC_SOURCES:
- RSSHub finance/news routes => https://docs.rsshub.app/routes/finance => USE_FOR: broad RSS route discovery for finance/news => SOURCE_STATE: dynamic_check_required
- NewsAPI => https://newsapi.org/docs => USE_FOR: live article search and source/domain filtering => SOURCE_STATE: dynamic_check_required
- SEC EDGAR data APIs => https://data.sec.gov/ => USE_FOR: official US company filings and XBRL facts => SOURCE_STATE: dynamic_check_required
- FRED API => https://fred.stlouisfed.org/docs/api/fred/ => USE_FOR: macroeconomic series, releases, categories => SOURCE_STATE: dynamic_check_required
- Alpha Vantage docs => https://www.alphavantage.co/documentation/ => USE_FOR: market data, fundamentals, market news and sentiment => SOURCE_STATE: dynamic_check_required
- Polygon stocks API => https://polygon.io/docs/rest/stocks/overview/ => USE_FOR: US stock market data, reference data, company news => SOURCE_STATE: dynamic_check_required
- Finnhub API docs => https://finnhub.io/docs/api => USE_FOR: market data, company news, sentiment, filings where available => SOURCE_STATE: dynamic_check_required

HIGH_PRIORITY_GITHUB_SOURCES:
- OpenBB-finance/OpenBB => https://github.com/OpenBB-finance/OpenBB => STARS: 67103 => PUSHED: 2026-05-06 => USE_FOR: financial data platform and AI-agent finance source map => SOURCE_STATE: source_index_dynamic
- DIYgod/RSSHub => https://github.com/DIYgod/RSSHub => STARS: 43866 => PUSHED: 2026-05-06 => USE_FOR: RSS route engine for news/finance/AI feeds => SOURCE_STATE: source_index_dynamic
- public-apis/public-apis => https://github.com/public-apis/public-apis => STARS: 432660 => PUSHED: 2026-05-05 => USE_FOR: API discovery, not factual truth => SOURCE_STATE: source_index_dynamic
- ranaroussi/yfinance => https://github.com/ranaroussi/yfinance => STARS: 23427 => PUSHED: 2026-05-05 => USE_FOR: Yahoo Finance market data access pattern => SOURCE_STATE: source_index_dynamic
- akfamily/akshare => https://github.com/akfamily/akshare => STARS: 18916 => PUSHED: 2026-05-02 => USE_FOR: China/global finance data interface map => SOURCE_STATE: source_index_dynamic
- WilsonFreitas/awesome-quant => https://github.com/wilsonfreitas/awesome-quant => STARS: 26027 => PUSHED: 2026-05-06 => USE_FOR: quant library/source discovery => SOURCE_STATE: source_index_dynamic
- microsoft/qlib => https://github.com/microsoft/qlib => STARS: 42095 => PUSHED: 2026-04-22 => USE_FOR: AI quant research platform reference => SOURCE_STATE: source_index_dynamic
- AI4Finance-Foundation/FinGPT => https://github.com/AI4Finance-Foundation/FinGPT => STARS: 19952 => PUSHED: 2026-04-24 => USE_FOR: financial LLM and sentiment architecture reference => SOURCE_STATE: source_index_dynamic
- AI4Finance-Foundation/FinRL => https://github.com/AI4Finance-Foundation/FinRL => STARS: 15078 => PUSHED: 2026-04-05 => USE_FOR: financial reinforcement learning reference => SOURCE_STATE: source_index_dynamic
- AI4Finance-Foundation/FinRobot => https://github.com/AI4Finance-Foundation/FinRobot => STARS: 6876 => PUSHED: 2026-04-03 => USE_FOR: financial AI agent workflow reference => SOURCE_STATE: source_index_dynamic
- dgunning/edgartools => https://github.com/dgunning/edgartools => STARS: 2102 => PUSHED: 2026-05-06 => USE_FOR: SEC EDGAR filings and XBRL access pattern => SOURCE_STATE: source_index_dynamic
- Shubhamsaboo/awesome-llm-apps => https://github.com/Shubhamsaboo/awesome-llm-apps => STARS: 109036 => PUSHED: 2026-05-04 => USE_FOR: AI agent/RAG app source discovery => SOURCE_STATE: source_index_dynamic
- dair-ai/ML-Papers-of-the-Week => https://github.com/dair-ai/AI-Papers-of-the-Week => STARS: 12393 => PUSHED: 2026-05-05 => USE_FOR: weekly AI/ML paper trend source => SOURCE_STATE: source_index_dynamic
- huggingface/transformers => https://github.com/huggingface/transformers => STARS: 160310 => PUSHED: 2026-05-06 => USE_FOR: model ecosystem trend signal => SOURCE_STATE: source_index_dynamic
- vllm-project/vllm => https://github.com/vllm-project/vllm => STARS: 79181 => PUSHED: 2026-05-06 => USE_FOR: LLM serving trend signal => SOURCE_STATE: source_index_dynamic

LOWER_PRIORITY_OR_CAUTION:
- RSSNext/Folo => high-star AI RSS reader; useful as product/reference, not source of factual truth
- RomelTorres/alpha_vantage => wrapper only; prefer official Alpha Vantage docs for live facts
- papers-we-love/papers-we-love => high-star but broad CS reading list, weak for current news
- Hannibal046/Awesome-LLM => useful LLM bibliography, pushed 2025-07-31 so lower freshness
- backtesting.py/quantstats/ffn => useful tooling, not current news or factual source

TRIGGER_ROUTING:
- breaking news/current events => RSSHub routes or NewsAPI first
- stock price/company news/sentiment => Polygon or Alpha Vantage or Finnhub, then cite timestamp
- SEC filing/fundamental facts => SEC EDGAR official API first; edgartools can guide access
- macro rates/inflation/jobs/yields => FRED API first
- AI product/repo trend => GitHub repo metadata plus official project docs
- AI papers => ML-Papers-of-the-Week plus original paper/source link

FINAL_SCAN:
- every current claim must include source URL and observed date/time
- never call stars or pushed_at permanent; re-check before saying "currently high-star" or "actively updated"
- do not import whole repos; import only this short source index or verified extracts
