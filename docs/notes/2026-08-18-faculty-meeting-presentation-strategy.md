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

## Literature Citations — Full Resource (added Aug 18 — Wilson)

Everything below is organized by the argument it backs, so it can be pulled straight into slides or the paper. Papers that support more than one argument are cross-listed with a "(also →)" tag. All URLs verified; papers marked ★ are new finds not yet in `Literature_Review_Map.docx` (the annotated 27-paper map, Wilson, Apr 23 — has fuller summaries + relevance notes for each).

**One-line positioning:** Prior work shows (1) network position predicts outcomes, (2) network analysis works in soccer at the tactical / within-game level, and (3) crowd sentiment and media text carry predictive signal. We are the first to combine all three — text-derived club co-occurrence networks → centrality → **preseason, season-level prediction** of athletic (Paper 1) and commercial (Paper 2) performance.

---

### Stream 1 — Network analysis as a predictive methodology (outside sports)
*Argument: a node's position in a network is a leading indicator of real-world outcomes. This is established in epidemiology, finance, and political behavior — we bring it to sports clubs.*

**Network position predicts outcomes**
- ★ **Christakis & Fowler (2010).** Social network sensors for early detection of contagious outbreaks. *PLoS ONE*, 5(9), e12948. https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0012948
  Central individuals get infected earlier; monitoring a high-centrality sample detected the 2009 Harvard flu outbreak **two weeks before** the population at large. Best "aha" example — centrality as an early-warning signal.
- ★ **Ahern (2013).** Network centrality and the cross section of stock returns. SSRN 2197370 (265+ cites). https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2197370
  Industries more central in the intersectoral trade network earn higher returns; shocks propagate through central nodes. Centrality is a priced, predictive attribute of an economic entity.
- ★ **Bond, Fariss, Jones, Kramer, Marlow, Settle & Fowler (2012).** A 61-million-person experiment in social influence and political mobilization. *Nature*, 489, 295–298. https://pubmed.ncbi.nlm.nih.gov/22972300/
  Facebook RCT during the 2010 US midterms: network transmission of a mobilization message drove **more real-world voting** than the message itself. Network structure predicts and shapes behavior at scale. (Prof. Tang's Facebook/voting example.)

**Text → network → prediction (methodologically closest to us)**
- ★ **Schwenkler & Zheng (2019).** The network of firms implied by the news. SSRN 3320859 / ESRB WP 108; forthcoming *J. Financial Stability*. https://www.esrb.europa.eu/pub/pdf/wp/esrb.wp108~40756dc3b5.en.pdf
  ML builds a firm network **from news co-mentions**; news-implied links yield predictable returns and downgrades, and connectivity shocks predict volatility, credit spreads, defaults, output declines. Same pipeline as ours, in finance. **Lead with this one.**
- **Özgür, Cetin & Bingol (2008).** Co-occurrence network of Reuters news. arXiv:0712.2491. https://arxiv.org/abs/0712.2491
  People co-mentioned in Reuters articles → small-world network; PageRank vs. degree tested for predicting entity importance. Same node/edge construction as ours.
- **Mihalcea & Tarau (2004).** TextRank: Bringing order into texts. EMNLP. https://aclanthology.org/W04-3252/
  PageRank applied to text graphs. Establishes graph-ranking on text as a standard method.

**Methods anchors (must-cite in Methods)**
- **Page, Brin, Motwani & Winograd (1998).** The PageRank citation ranking. Stanford InfoLab. http://ilpubs.stanford.edu:8090/422/
- **Freeman (1979).** Centrality in social networks: Conceptual clarification. *Social Networks*, 1(3), 215–239. https://www.sciencedirect.com/science/article/abs/pii/0378873378900217
- **Newman (2010).** *Networks: An Introduction*. OUP. https://global.oup.com/academic/product/networks-9780198805090

---

### Stream 2 — Network analysis in sports
*Argument: network science is already accepted in soccer — but only for player-to-player passing networks within matches. We move the unit of analysis from players-in-a-game to clubs-in-the-media-ecosystem, and the horizon from a match to a season.*

**Passing networks (tactical / within-game)**
- **Grund (2012).** Network structure and team performance: The case of English Premier League soccer teams. *Social Networks*, 34(4), 682–690. https://www.sciencedirect.com/science/article/abs/pii/S0378873312000500
  283,259 passes, 23 EPL teams, mixed-effects models. Higher passing intensity → better performance; more centralized networks → worse. **The anchor cite** — and the paper that makes our gap visible (on-field networks studied; narrative networks not).
- **Pina, Paulo & Araújo (2017).** Network characteristics of successful performance in association football: UEFA Champions League. *Frontiers in Psychology*, 8, 1173. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2017.01173/full
  Density, centralization, clustering **predict** the outcome of offensive plays. Replicates Grund at possession level.
- **Buldú et al. (2018).** Using network science to analyse football passing networks: Dynamics, space, time, and the multilayer nature of the game. *Frontiers in Psychology*, 9, 1900. https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2018.01900/full
  Field review; establishes temporal evolution of networks as a studied dimension (supports our yearly network construction).

**Social-media networks in sports (bridge to Stream 3)**
- **Miranda-Peña, Ceballos, Hervert-Escobar & Gonzalez-Mendoza (2021).** Predicting soccer results through sentiment analysis: A graph theory approach. Springer. https://link.springer.com/chapter/10.1007/978-3-030-77980-1_32
  Twitter graph; **club/fan network centrality as a feature predicting EPL match outcomes** (81% acc.). Closest sports precedent for centrality-as-predictor. (also → Stream 3)
- **Yan, Watanabe, Shapiro, Naraine & Hull (2019).** Unfolding the Twitter scene of the 2017 UEFA Champions League Final: social media networks and power dynamics. *European Sport Management Quarterly*. https://www.tandfonline.com/doi/abs/10.1080/16184742.2018.1517272
  Network analysis of sports social-media discourse in a sport-management journal — shows the method is publishable in our target outlets. Descriptive, not predictive.

**Sports prediction baseline (what the field predicts with, and what's missing)**
- **Bunker & Susnjak (2022).** The application of machine learning techniques for predicting match results in team sport: A review. *JAIR*, 73, 1285–1322. https://www.jair.org/index.php/jair/article/view/13509
  Review 1996–2019: models rely on on-field data; media/fan discourse absent as features. **Soccer is harder to predict** than other sports (low scoring, high variance) → motivates novel signals. Cite to establish the gap.
- **Anzer & Bauer (2021).** A goal scoring probability model … (xG). *Frontiers in Sports and Active Living*. https://www.frontiersin.org/articles/10.3389/fspor.2021.624475/full — xG as the standard process-performance measure (we use ASA xG as a control).
- **Knoll & Stübinger (2020).** Machine-learning-based statistical arbitrage football betting. *KI – Künstliche Intelligenz*. https://link.springer.com/article/10.1007/s13218-019-00610-4 — ML match prediction across the top-5 leagues framed as arbitrage.
- ★ **Forrest, Goddard & Simmons (2005).** Odds-setters as forecasters: The case of English football. *Int. J. Forecasting*, 21(3), 551–564. https://www.sciencedirect.com/science/article/abs/pii/S0169207005000300
  Bookmaker odds are efficient forecasters. **The benchmark to beat** — expect this question from Andy's family (betting / analytics). If centrality adds signal beyond odds/wages, that's the headline; if not, odds are the ceiling.

---

### Stream 3 — Crowd sentiment & media text as predictors ("wisdom of crowds")
*Argument: collective public attention and expectations, expressed in press and social media, contain information about future outcomes. Established in finance; emerging in sports. Our centrality score is a structural summary of that collective signal.*

**Sports: social-media sentiment predicts results**
- **Schumaker, Jarmoszko & Labedz (2016).** Predicting wins and spread in the Premier League using a sentiment analysis of Twitter. *Decision Support Systems*, 88, 76–84. https://www.sciencedirect.com/science/article/abs/pii/S0167923616300835
  Twitter sentiment on the 20 EPL clubs predicts match outcomes and spread; **explicitly framed as wisdom of crowds**. Our single closest precursor — cite prominently. We extend it: Twitter → press + Reddit; sentiment → network centrality; match → season.
- **Godin, Zuallaert, Vandersmissen, De Neve & Van de Walle (2014).** Beating the bookmakers: Leveraging statistics and Twitter microposts for predicting soccer results. https://www.researchgate.net/publication/264977879
  50M+ tweets (volume, sentiment, user predictions) + stats beat bookmaker baselines on EPL results.
- **Frigau, Contu, Mola & Conversano (2024).** The game beyond the field: football players' performance through social media, sentiment and topic analysis. *Computational Statistics*. https://link.springer.com/article/10.1007/s00180-024-01584-0
  167,841 tweets on 512 EPL players; pre-match sentiment linked to post-match performance (PLS-PM). Recent — shows the stream is active.
- **Miranda-Peña et al. (2021)** — (also → Stream 2) sentiment + graph centrality → match outcomes.

**Finance: the canonical "text predicts outcomes" literature**
- **Tetlock (2007).** Giving content to investor sentiment: The role of media in the stock market. *Journal of Finance*, 62(3), 1139–1168. https://business.columbia.edu/sites/default/files-efs/pubfiles/3097/Tetlock_Media_Sentiment_JF.pdf
  WSJ column pessimism predicts downward price pressure and volume. Seminal media-sentiment-as-predictor paper.
- **Bollen, Mao & Zeng (2011).** Twitter mood predicts the stock market. *J. Computational Science*, 2(1), 1–8. https://arxiv.org/abs/1010.3003
  Collective Twitter mood predicts DJIA direction (~87% claimed). Most-cited crowd-mood → outcome paper.
- **Antweiler & Frank (2004).** Is all that talk just noise? The information content of internet stock message boards. *Journal of Finance*, 59(3), 1259–1294. https://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.2004.00662.x
  1.5M Yahoo Finance / Raging Bull posts predict volatility and volume. Message boards ≈ our Reddit corpus.
- **Loughran & McDonald (2011).** When is a liability not a liability? Textual analysis, dictionaries, and 10-Ks. *Journal of Finance*, 66(1), 35–65. https://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.2010.01625.x
  Domain-specific sentiment dictionaries beat generic ones. Methods cite for our sentiment scoring / VADER caveats.

**Attention as a measurable, predictive quantity**
- ★ **Da, Engelberg & Gao (2011).** In search of attention. *Journal of Finance*, 66(5), 1461–1499. https://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.2011.01679.x
  Google Search Volume Index as a direct measure of attention; predicts short-run price pressure and IPO returns. Justifies our Google Trends variable and the "collective attention → outcome" framing.
- ★ **Choi & Varian (2012).** Predicting the present with Google Trends. *Economic Record*, 88(s1), 2–9. https://onlinelibrary.wiley.com/doi/10.1111/j.1475-4932.2012.00809.x
  Search data nowcasts economic indicators. Foundational "public attention as forecast input."

**Media reputation predicts organizational performance** — (also → Stream 4; this is why Track 4 also belongs here)
- **Deephouse (2000).** Media reputation as a strategic resource: An integration of mass communication and resource-based theories. *Journal of Management*, 26(6), 1091–1112. https://journals.sagepub.com/doi/10.1177/014920630002600602
  Defines "media reputation" (overall evaluation of a firm in the media) and shows it **predicts financial performance** (ROA) in a panel of commercial banks. Directly analogous: media standing → firm outcomes.
- **Fombrun & Shanley (1990).** What's in a name? Reputation building and corporate strategy. *Academy of Management Journal*, 33(2), 233–258. https://journals.aom.org/doi/10.5465/256324
  Media exposure and visibility shape corporate reputation, which relates to performance.

**Why media coverage reflects collective expectations (theory)**
- ★ **McCombs & Shaw (1972).** The agenda-setting function of mass media. *Public Opinion Quarterly*, 36(2), 176–187. https://doi.org/10.1086/267990
  Media salience ↔ public salience. Theoretical basis for treating press co-occurrence as a proxy for collective attention/expectations — the "wisdom of crowds" mechanism Prof. Tang proposed.

---

### Stream 4 — Narrative / media attention as an organizational resource
*Argument (mainly Paper 2, commercial returns; and the Discussion of Paper 1): even where narrative centrality does not move on-field results, it is a distinct strategic resource that clubs and investors should manage. This is what makes the MLS "decoupling" finding interesting rather than null.*

**Resource-Based View**
- **Barney (1991).** Firm resources and sustained competitive advantage. *Journal of Management*, 17(1), 99–120. https://journals.sagepub.com/doi/10.1177/014920639101700108 — VRIN resources; narrative capital as valuable, rare, hard to imitate.
- **Wernerfelt (1984).** A resource-based view of the firm. *Strategic Management Journal*, 5(2), 171–180. https://onlinelibrary.wiley.com/doi/10.1002/smj.4250050207 — original RBV.

**Media reputation as a resource** — (also → Stream 3)
- **Deephouse (2000)** and **Fombrun & Shanley (1990)** — see Stream 3. Media reputation is both a *predictor* (Stream 3) and a *resource* (Stream 4).

**Sponsorship / commercial value of attention**
- **Cornwell, Weeks & Roy (2005).** Sponsorship-linked marketing: Opening the black box. *Journal of Advertising*, 34(2), 21–42. https://www.tandfonline.com/doi/abs/10.1080/00913367.2005.10639194 — sponsors borrow the equity/attention of the property; centrality is what they're buying.
- **Meenaghan (2001).** Understanding sponsorship effects. *Psychology & Marketing*, 18(2), 95–122. https://onlinelibrary.wiley.com/doi/10.1002/1520-6793(200102)18:2%3C95::AID-MAR1001%3E3.0.CO;2-H — image transfer, goodwill, fan identification.
- **Biscaia, Correia, Rosado, Ross & Maroco (2013).** Sport sponsorship: team loyalty, sponsorship awareness, attitude toward the sponsor, and purchase intentions. *Journal of Sport Management*, 27(4), 288–302. https://journals.humankinetics.com/view/journals/jsm/27/4/article-p288.xml — fan-side mechanism linking attention to revenue.

---

### Additional streams to consider (not yet in the lit map)

- **Sports economics wage–performance baseline** — Szymanski & Kuypers (1999) *Winners and Losers*; Kuper & Szymanski *Soccernomics*. Wages explain most of league-table variance; our claim is incremental signal beyond wages/transfers (this is exactly what the EPL-Panel controls are for). *[Books — verify editions before citing.]*
- **Social influence / contagion in networks** — Aral & Walker (2012) *Science* "Identifying influential and susceptible members of social networks"; Ugander, Backstrom, Marlow & Kleinberg (2012) *PNAS* "Structural diversity in social contagion." Further Facebook-scale evidence that network structure predicts adoption/behavior. *[From memory — verify before citing.]*
- **Prediction markets / wisdom of crowds** — Surowiecki (2004) *The Wisdom of Crowds*; Wolfers & Zitzewitz (2004) "Prediction markets," *J. Economic Perspectives*. Popular + academic anchor for the framing Prof. Tang suggested. *[Verify.]*
- **Bandwagon / attention–demand in sports** — attendance and TV-demand literature (e.g., Borland & Macdonald 2003, "Demand for sport," *Oxford Review of Economic Policy*). Links media attention to commercial outcomes for Paper 2. *[Verify.]*

**Suggested slide mapping:** Stream 1 → "why network position predicts" (Christakis flu; Schwenkler news network); Stream 2 → "networks already work in soccer, but only within games" (Grund); Stream 3 → "the crowd knows" (Schumaker; Bollen; Deephouse); Stream 4 → "why it matters even when it doesn't win games" (Barney; Cornwell).
