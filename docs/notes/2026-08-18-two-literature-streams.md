# Two Literature Streams — Citations for the Aug 19 Meeting with Andy

Response to the action item in `2026-08-18-faculty-meeting-presentation-strategy.md`:
> find and cite the two supporting streams (network prediction studies + sports passing networks).

Positioning: prior sports work validates network analysis at a tactical / within-game level;
our research extends it to aggregate, preseason, season-level prediction.

---

## Stream 1 — Network analysis as a predictive methodology (non-sports)

**Christakis, N. A., & Fowler, J. H. (2010).** Social network sensors for early detection of contagious outbreaks. *PLoS ONE*, 5(9), e12948.
https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0012948
- Individuals near the center of a social network get infected earlier than those on the periphery. Monitoring a "friends of random people" sample (higher centrality) during the 2009 H1N1 outbreak at Harvard detected the flu epidemic **two weeks in advance** of the general population.
- Talking point: position in a network is a *leading indicator* of an outcome — the same logic as club centrality predicting next-season performance.

**Ahern, K. R. (2013).** Network centrality and the cross section of stock returns. Working paper (SSRN 2197370). Cited 265+.
https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2197370
- Industries more central in the network of intersectoral trade earn higher stock returns; central nodes have greater exposure to shocks transmitted through the network.
- Talking point: centrality as a priced, predictive attribute of an economic entity — not just a descriptive statistic.

**Schwenkler, G., & Zheng, H. (2019).** The network of firms implied by the news. SSRN 3320859 / ESRB Working Paper 108; forthcoming *Journal of Financial Stability*.
https://www.esrb.europa.eu/pub/pdf/wp/esrb.wp108~40756dc3b5.en.pdf
- Builds a firm network **from news text co-mentions** (ML on articles → firm network). News-implied links yield predictable returns and downgrades; shocks to news-implied connectivity predict increases in volatility, credit spreads, default rates, and declines in output.
- Talking point: methodologically the closest analogue to our work — text co-occurrence → network → prediction of real-world outcomes, in finance rather than sports.

## Stream 2 — Network analysis already used in sports (already in Literature_Review_Map.docx)

**Grund, T. U. (2012).** Network structure and team performance: The case of English Premier League soccer teams. *Social Networks*, 34(4), 682–690.
https://www.sciencedirect.com/science/article/abs/pii/S0378873312000500
- 283,259 passes, 23 EPL teams. Higher passing intensity → better performance; more centralized passing networks → worse performance. Foundational cite for network analysis in soccer.

**Pina, T. J., Paulo, A., & Araújo, D. (2017).** Network characteristics of successful performance in association football: A study on the UEFA Champions League. *Frontiers in Psychology*, 8, 1173.
- Team network density, centralization, and clustering predict the outcome of offensive plays.

**Bonus (bridges both streams):** Miranda-Peña et al. (2021), *Predicting Soccer Results Through Sentiment Analysis: A Graph Theory Approach* — Twitter graph, club/fan network centrality as a feature predicting EPL match outcomes (81% accuracy). Sports, but network → prediction.
