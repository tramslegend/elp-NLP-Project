# Faculty Meeting — Sports Analytics Presentation & Paper Strategy

**Date:** August 18, 2026
**Topic:** Presentation strategy and prep for the Aug 19 meeting with Andy

---

## Presentation Strategy Advice

- **Make the audience feel smart.** Simplify complex work so they get an "aha" moment — people credit themselves for understanding, then become receptive to the pitch.
- **Never defend the work like it's personal when challenged.** Acknowledge the question warmly first, then reframe it as a collaborative discussion. Defensiveness alienates the questioner no matter how well-reasoned the answer is.
- **Sell the value, not a technical detail dump.**
  - Data section: explain the integration challenge, then show that we automated the solution.
  - Model section: teach AUC visually — ask the audience which curve is better and let them feel the win.
- **Bragging formula (two parts only):**
  1. Here is the hard problem we faced.
  2. Here is the smart thing we built to solve it.

## Meeting Prep — Aug 19, 12:30 PM with Andy

- Andy is low-key and is not expecting a formal academic presentation.
- Andy's wife is CMO of a sports analytics company, and his son works at a sports betting platform in Florida. Both may attend — good networking opportunity for introductions in the sports space.
- **Suggested structure:**
  1. Dante and Wilson open with background, purpose, and network formulation.
  2. Professor takes over to cover how centrality metrics predict Premier League performance.

## Key Narrative

**Why does network centrality have predictive power?**

Proposed framing: "wisdom of crowds" — news coverage reflects collective public attention and expectations, and that collective signal manifests in centrality scores.

## Literature to Cite (two streams)

1. **Network analysis as a predictive methodology** — e.g., early Facebook studies predicting voting behavior and music taste.
2. **Network analysis already used in sports** — e.g., passing networks in soccer.

**Positioning:** prior work validates the method at a tactical / within-game level; this research extends it to aggregate, preseason, season-level prediction.

## Action Items

- [ ] **Slides & talking points** — Dante and Wilson cover network formulation and centrality; send the slide link the night before for comments ahead of the 12:30 PM meeting.
- [ ] **Literature citations** — find and cite the two supporting streams above (network prediction studies + sports passing networks).

---

## Literature Citations (added Aug 18 — Wilson)

Positioning for all three streams: prior work validates (a) network position as a predictive signal, (b) network analysis in soccer at the tactical / within-game level, and (c) crowd sentiment and media text as predictive of outcomes. We combine all three and move to **aggregate, preseason, season-level prediction of club performance**.

### Stream 1 — Network analysis as a predictive methodology (non-sports)

- **Christakis & Fowler (2010).** Social network sensors for early detection of contagious outbreaks. *PLoS ONE*, 5(9), e12948. https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0012948
  Central individuals in a social network get infected earlier; monitoring a high-centrality "friends" sample detected the 2009 Harvard flu outbreak **two weeks in advance**. Network position as a leading indicator.
- **Ahern (2013).** Network centrality and the cross section of stock returns. SSRN 2197370. https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2197370
  Industries more central in the intersectoral trade network earn higher stock returns; shocks propagate through central nodes. Centrality as a priced, predictive attribute.
- **Schwenkler & Zheng (2019).** The network of firms implied by the news. SSRN 3320859 / ESRB WP 108; forthcoming *J. Financial Stability*. https://www.esrb.europa.eu/pub/pdf/wp/esrb.wp108~40756dc3b5.en.pdf
  Firm network built **from news co-mentions**; news-implied links predict returns and downgrades, and connectivity shocks predict volatility, credit spreads, defaults. Closest methodological analogue to our pipeline (text co-occurrence → network → prediction).
- **Özgür, Cetin & Bingol (2008).** Co-occurrence network of Reuters news. arXiv:0712.2491. https://arxiv.org/abs/0712.2491
  People co-mentioned in Reuters articles form a small-world network; PageRank/degree used to predict entity importance. Same construction as ours, applied to news.
- Methods anchors: **Page, Brin, Motwani & Winograd (1998)** — PageRank; **Freeman (1979)** — centrality measures.

### Stream 2 — Network analysis in sports (passing networks; tactical / within-game)

- **Grund (2012).** Network structure and team performance: The case of English Premier League soccer teams. *Social Networks*, 34(4), 682–690. https://www.sciencedirect.com/science/article/abs/pii/S0378873312000500
  283,259 passes, 23 EPL teams. Higher passing intensity → better performance; more centralized networks → worse. Foundational cite.
- **Pina, Paulo & Araújo (2017).** Network characteristics of successful performance in association football: UEFA Champions League. *Frontiers in Psychology*, 8, 1173. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2017.01173/full
  Density, centralization, clustering predict the outcome of offensive plays.
- **Buldú et al. (2018).** Using network science to analyse football passing networks. *Frontiers in Psychology*, 9, 1900. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2018.01900/full
  Review of the field: topology, space, time, multilayer structure.
- **Miranda-Peña et al. (2021).** Predicting soccer results through sentiment analysis: A graph theory approach. Springer. https://link.springer.com/chapter/10.1007/978-3-030-77980-1_32
  Twitter graph; **club/fan network centrality as a feature predicting EPL match outcomes** (81% accuracy). Bridges Streams 1–3.
- **Yan et al. (2019).** Twitter networks around the 2017 UCL Final: social media networks and power dynamics. *European Sport Management Quarterly*. https://www.tandfonline.com/doi/abs/10.1080/16184742.2018.1517272

### Stream 3 — Crowd sentiment & media text as predictors ("wisdom of crowds")

Sports:
- **Schumaker, Jarmoszko & Labedz (2016).** Predicting wins and spread in the Premier League using a sentiment analysis of Twitter. *Decision Support Systems*. https://www.sciencedirect.com/science/article/abs/pii/S0167923616300835
  Twitter sentiment on the 20 EPL clubs predicts match outcomes; explicitly framed as wisdom of crowds. Our closest precursor.
- **Godin et al. (2014).** Beating the bookmakers: Leveraging statistics and Twitter microposts for predicting soccer results. https://www.researchgate.net/publication/264977879
  50M+ tweets combined with stats to predict EPL results.
- **Frigau et al. (2024).** The game beyond the field: football players' performance through social media, sentiment and topic analysis. *Computational Statistics*. https://link.springer.com/article/10.1007/s00180-024-01584-0
  Pre-match sentiment linked to post-match player performance.

Finance (the canonical "text predicts outcomes" literature):
- **Tetlock (2007).** Giving content to investor sentiment: The role of media in the stock market. *Journal of Finance*. https://business.columbia.edu/sites/default/files-efs/pubfiles/3097/Tetlock_Media_Sentiment_JF.pdf
  WSJ column pessimism predicts downward pressure on market prices.
- **Bollen, Mao & Zeng (2011).** Twitter mood predicts the stock market. *J. Computational Science*. https://arxiv.org/abs/1010.3003
  Collective Twitter mood predicts DJIA direction.
- **Antweiler & Frank (2004).** Is all that talk just noise? The information content of internet stock message boards. *Journal of Finance*. https://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.2004.00662.x
  1.5M message-board posts predict volatility and volume.
- **Loughran & McDonald (2011).** When is a liability not a liability? *Journal of Finance*. Domain-specific sentiment dictionaries (methods cite for our sentiment scoring).

### Other streams worth considering (not yet in the lit map)

- **Attention / search-volume prediction** — Choi & Varian (2012) "Predicting the present with Google Trends" (*Economic Record*); Da, Engelberg & Gao (2011) "In search of attention" (*J. Finance*). Supports the "collective public attention carries signal" framing and gives a benchmark for our Google Trends variable.
- **Betting-market efficiency as the benchmark to beat** — Forrest, Goddard & Simmons (2005) "Odds-setters as forecasters: The case of English football" (*Int. J. Forecasting*). If centrality adds information beyond bookmaker odds, that's a strong claim; if not, still a useful ceiling.
- **Agenda-setting / media attention theory** — McCombs & Shaw (1972) "The agenda-setting function of mass media" (*Public Opinion Quarterly*). Theoretical basis for why press co-occurrence reflects collective expectations.
- **Media reputation as a strategic resource** — Deephouse (2000), Fombrun & Shanley (1990), Barney (1991) — already Track 4 of the lit map; explains why narrative centrality can matter for the *commercial* paper even when it doesn't move on-field results.
- **Sports economics wage–performance baseline** — Szymanski & Kuypers (1999) *Winners and Losers*; Kuper & Szymanski *Soccernomics*. Wages explain most of the league-table variance; our claim is that centrality adds signal beyond wages/transfers.

Full annotated map with all 27 papers: `Literature_Review_Map.docx` (Wilson, Apr 23).
