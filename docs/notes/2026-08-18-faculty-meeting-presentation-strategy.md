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

## Academic Evidence for What We Built (added Aug 18 — Wilson)

Our part of the presentation answers four questions with academic backing. Each paper below: title, then one sentence on why it's evidence for us. Full annotated summaries for the older ones are in `Literature_Review_Map.docx` (Wilson, Apr 23).

### 1. Has network analysis been used in sports?

- **Grund (2012) — Network structure and team performance: The case of English Premier League soccer teams.** *Social Networks.* https://www.sciencedirect.com/science/article/abs/pii/S0378873312000500
  Foundational soccer network paper (283k passes, 23 EPL teams); shows passing-network structure predicts team performance — and because it studies players within games, it makes our gap obvious: nobody has applied networks to clubs in the media.
- **Pina, Paulo & Araújo (2017) — Network Characteristics of Successful Performance in Association Football: A Study on the UEFA Champions League.** *Frontiers in Psychology.* https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2017.01173/full
  Network density and centralization predict outcomes of offensive plays; shows the Grund result holds across competitions.
- **Buldú et al. (2018) — Using Network Science to Analyse Football Passing Networks: Dynamics, Space, Time, and the Multilayer Nature of the Game.** *Frontiers in Psychology.* https://www.frontiersin.org/journals/psychology/articles/10.3389/fpsyg.2018.01900/full
  Review of the whole soccer-network field; proves the method is established in soccer and that tracking networks over time (as we do yearly) is accepted practice.
- **Miranda-Peña et al. (2021) — Predicting Soccer Results Through Sentiment Analysis: A Graph Theory Approach.** Springer. https://link.springer.com/chapter/10.1007/978-3-030-77980-1_32
  Uses club/fan network centrality from Twitter as a feature to predict EPL match results (81% accuracy); the closest sports precedent for centrality-as-predictor.
- **Yan et al. (2019) — Unfolding the Twitter scene of the 2017 UEFA Champions League Final: social media networks and power dynamics.** *European Sport Management Quarterly.* https://www.tandfonline.com/doi/abs/10.1080/16184742.2018.1517272
  Network analysis of sports social-media discourse published in a sport-management journal; shows our approach fits our target outlets.
- **Bunker & Susnjak (2022) — The Application of Machine Learning Techniques for Predicting Match Results in Team Sport: A Review.** *JAIR.* https://www.jair.org/index.php/jair/article/view/13509
  Reviews 20+ years of sports prediction and finds models rely almost entirely on on-field data — media and fan discourse are absent — which is the gap we fill; also notes soccer is unusually hard to predict, motivating new signals.
- **Forrest, Goddard & Simmons (2005) — Odds-setters as forecasters: The case of English football.** *International Journal of Forecasting.* https://www.sciencedirect.com/science/article/abs/pii/S0169207005000300
  Bookmaker odds are efficient forecasters of results; this is the benchmark any new predictor has to add to — expect this question from Andy's family.

### 2. Has network analysis been used for prediction (outside sports)?

- **Christakis & Fowler (2010) — Social Network Sensors for Early Detection of Contagious Outbreaks.** *PLoS ONE.* https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0012948
  Central people in a social network caught the 2009 flu earlier, so watching a high-centrality group predicted the outbreak two weeks ahead; cleanest example that network position is a leading indicator.
- **Bond et al. (2012) — A 61-Million-Person Experiment in Social Influence and Political Mobilization.** *Nature.* https://pubmed.ncbi.nlm.nih.gov/22972300/
  Facebook experiment where network transmission drove more real-world voting than the message itself; shows network structure predicts and shapes behavior at scale.
- **Ahern (2013) — Network Centrality and the Cross Section of Stock Returns.** SSRN. https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2197370
  Industries more central in the trade network earn higher stock returns; centrality is a priced, predictive attribute of an economic entity — same claim we make for clubs.
- **Schwenkler & Zheng (2019) — The Network of Firms Implied by the News.** SSRN / ESRB WP; forthcoming *J. Financial Stability.* https://www.esrb.europa.eu/pub/pdf/wp/esrb.wp108~40756dc3b5.en.pdf
  Builds a firm network from news co-mentions and shows it predicts returns, downgrades, and defaults; this is our exact pipeline (text co-occurrence → network → prediction) applied in finance.
- **Özgür, Cetin & Bingol (2008) — Co-occurrence Network of Reuters News.** arXiv. https://arxiv.org/abs/0712.2491
  People co-mentioned in news articles form a network whose PageRank/degree predicts real-world importance; same node/edge construction we use.

### 3. Can crowd sentiment / media discourse be used for prediction — and is it a valuable resource?

**As a predictor (why we build the network from press and Reddit):**
- **Schumaker, Jarmoszko & Labedz (2016) — Predicting wins and spread in the Premier League using a sentiment analysis of twitter.** *Decision Support Systems.* https://www.sciencedirect.com/science/article/abs/pii/S0167923616300835
  Twitter sentiment about EPL clubs predicts match results and is framed as wisdom of crowds; our single closest precursor — we extend it from tweets/matches to press+Reddit networks/seasons.
- **Godin et al. (2014) — Beating the Bookmakers: Leveraging Statistics and Twitter Microposts for Predicting Soccer Results.** https://www.researchgate.net/publication/264977879
  50M+ tweets combined with stats beat bookmaker baselines on EPL results; shows crowd text adds information beyond the market.
- **Frigau et al. (2024) — The game beyond the field: on football players' performance through social media, sentiment and topic analysis.** *Computational Statistics.* https://link.springer.com/article/10.1007/s00180-024-01584-0
  Pre-match Twitter sentiment on 512 EPL players links to post-match performance; recent proof the stream is active.
- **Tetlock (2007) — Giving Content to Investor Sentiment: The Role of Media in the Stock Market.** *Journal of Finance.* https://business.columbia.edu/sites/default/files-efs/pubfiles/3097/Tetlock_Media_Sentiment_JF.pdf
  Newspaper column sentiment predicts stock-market moves; the seminal proof that press text carries predictive information.
- **Bollen, Mao & Zeng (2011) — Twitter mood predicts the stock market.** *Journal of Computational Science.* https://arxiv.org/abs/1010.3003
  Collective Twitter mood predicts the Dow; the most-cited "crowd mood predicts outcomes" paper.
- **Antweiler & Frank (2004) — Is All That Talk Just Noise? The Information Content of Internet Stock Message Boards.** *Journal of Finance.* https://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.2004.00662.x
  1.5M message-board posts predict volatility and volume; message boards are the direct analogue of our Reddit corpus.
- **Da, Engelberg & Gao (2011) — In Search of Attention.** *Journal of Finance.* https://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.2011.01679.x
  Google search volume as a direct measure of public attention that predicts prices; backs our Google Trends variable and the "collective attention carries signal" idea.
- **Choi & Varian (2012) — Predicting the Present with Google Trends.** *Economic Record.* https://onlinelibrary.wiley.com/doi/10.1111/j.1475-4932.2012.00809.x
  Search data forecasts economic indicators; foundational "public attention as forecast input."
- **McCombs & Shaw (1972) — The Agenda-Setting Function of Mass Media.** *Public Opinion Quarterly.* https://doi.org/10.1086/267990
  Media salience mirrors public salience; the theory for why press co-occurrence is a proxy for collective expectations (the wisdom-of-crowds mechanism Prof. Tang proposed).
- **Deephouse (2000) — Media Reputation as a Strategic Resource: An Integration of Mass Communication and Resource-Based Theories.** *Journal of Management.* https://journals.sagepub.com/doi/10.1177/014920630002600602
  Defines media reputation and shows it predicts firm financial performance (bank ROA); media standing → organizational outcomes, and it's also a resource (below).
- **Fombrun & Shanley (1990) — What's in a Name? Reputation Building and Corporate Strategy.** *Academy of Management Journal.* https://journals.aom.org/doi/10.5465/256324
  Media exposure shapes corporate reputation, which relates to performance.
- **Loughran & McDonald (2011) — When Is a Liability Not a Liability? Textual Analysis, Dictionaries, and 10-Ks.** *Journal of Finance.* https://onlinelibrary.wiley.com/doi/10.1111/j.1540-6261.2010.01625.x
  Domain-specific sentiment dictionaries beat generic ones; methods backing for how we score sentiment.

**As a valuable resource (why narrative matters even when it doesn't win games — Paper 2 / Discussion):**
- **Barney (1991) — Firm Resources and Sustained Competitive Advantage.** *Journal of Management.* https://journals.sagepub.com/doi/10.1177/014920639101700108
  Resource-Based View: narrative capital is valuable, rare, and hard to imitate — a strategic resource in its own right.
- **Wernerfelt (1984) — A Resource-Based View of the Firm.** *Strategic Management Journal.* https://onlinelibrary.wiley.com/doi/10.1002/smj.4250050207
  Original RBV; frames clubs by their resource profile, not just results.
- **Cornwell, Weeks & Roy (2005) — Sponsorship-Linked Marketing: Opening the Black Box.** *Journal of Advertising.* https://www.tandfonline.com/doi/abs/10.1080/00913367.2005.10639194
  Sponsors buy the attention/equity of a property; centrality is a measure of what they're buying.
- **Meenaghan (2001) — Understanding Sponsorship Effects.** *Psychology & Marketing.* https://onlinelibrary.wiley.com/doi/10.1002/1520-6793(200102)18:2%3C95::AID-MAR1001%3E3.0.CO;2-H
  Explains how sponsorship converts attention into consumer attitudes; supports the commercial-value argument.
- **Biscaia et al. (2013) — Sport Sponsorship: The Relationship Between Team Loyalty, Sponsorship Awareness, Attitude Toward the Sponsor, and Purchase Intentions.** *Journal of Sport Management.* https://journals.humankinetics.com/view/journals/jsm/27/4/article-p288.xml
  Fan-side evidence linking attention to revenue.

### 4. Is network analysis itself a sound, established method? (methods backing)

- **Page, Brin, Motwani & Winograd (1998) — The PageRank Citation Ranking: Bringing Order to the Web.** http://ilpubs.stanford.edu:8090/422/
  The PageRank paper; mandatory cite for our centrality measure.
- **Freeman (1979) — Centrality in Social Networks: Conceptual Clarification.** *Social Networks.* https://www.sciencedirect.com/science/article/abs/pii/0378873378900217
  Defines degree/betweenness/closeness centrality; the vocabulary we use.
- **Mihalcea & Tarau (2004) — TextRank: Bringing Order into Texts.** EMNLP. https://aclanthology.org/W04-3252/
  PageRank applied to text graphs; precedent for graph ranking on text data.
- **Newman (2010) — Networks: An Introduction.** OUP. https://global.oup.com/academic/product/networks-9780198805090
  Standard textbook reference for network science.

### Possible additions (not yet verified — check before citing)
- Szymanski & Kuypers (1999) *Winners and Losers*; Kuper & Szymanski *Soccernomics* — wages explain most of league performance; our claim is centrality adds signal beyond wages.
- Aral & Walker (2012) *Science*; Ugander et al. (2012) *PNAS* — more Facebook-scale evidence that network structure predicts behavior.
- Surowiecki (2004) *The Wisdom of Crowds*; Wolfers & Zitzewitz (2004) *J. Econ. Perspectives* — anchors for the wisdom-of-crowds framing.
