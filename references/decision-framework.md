# Second-pass decision framework

Use this framework as a decision aid, not a rigid universal score. Adapt thresholds to the product economics and source scope, and expose any material assumption.

## 1. Source capability and graceful degradation

| Available evidence | Safe conclusions | Important limitations |
|---|---|---|
| Market analysis only | Market scale, aggregate trend, concentration, price/rating/newness structure | Weak ASIN-level entry and lifecycle evidence |
| Competitor detail only | Current competitor distribution, product/category boundary, new-listing performance | Cannot establish full market size or historical stability |
| ASIN history only | Lifecycle and price-sales behavior of the supplied cohort | Cannot represent current total market; sample-selection and survivorship bias |
| Market + competitor | Strong current-market and entry assessment | Historical persistence remains less certain |
| Market + history | Scale/trend plus cohort persistence | Current competitor quality and entry distribution may be incomplete |
| Competitor + history | Current cross-section plus cohort lifecycle | Overall market sizing and aggregate demand trend remain uncertain |
| All three | Full second-pass evidence | Still not supplier-, patent-, compliance- or order-ready |

When sources are missing, distinguish `cannot calculate` from `calculated with lower confidence`.

## 2. Market-boundary checks

Record:

- search/filter terms used;
- relevant ASIN count and relevant share;
- unique parent count after deduplication;
- top-seller coverage;
- involved source subcategories;
- adjacent-product contamination rate;
- target ASIN inclusion.

Use title-indicated core function and purchase purpose as the primary boundary. Use form, installation and scenario to split materially different buying decisions. Category dispersion is a warning to inspect, not automatic proof of multiple markets.

Do not force a broad-market layer when the exact product already represents an independent purchase intent. Expand outward only to test material upstream traffic, substitutes or sparse-sample uncertainty, and keep that evidence non-additive. A detailed user direction defines the decision object but does not suppress contradictory or adjacent evidence that could reverse the decision.

## 3. Demand and stability

Prefer complete monthly periods and show both aggregate scale and distribution.

Evaluate:

- latest complete month and trailing three-month level;
- month-over-month direction without treating one change as a trend;
- peak-month share of the observed period;
- volatility and whether the movement is broad across parents;
- search-demand confirmation when available;
- seasonality or event dependence;
- median, 25th and 75th percentile rather than averages alone.

If fewer than six complete market months exist, label stability confidence low or medium even when current demand is large. A newly emerging market can still enter third round conditionally.

For an emerging product, distinguish `evidence confidence` from `opportunity value`. Short history reduces the former. It does not by itself reduce the latter or justify waiting when delay could close a fast-copy window.

## 4. New-product entry probability

Group listings by age:

- `0-3 months`: launch velocity only;
- `4-6 months`: early retention and post-launch decay;
- `over 6 months`: persistence and mature competition.

When most relevant listings are under six months old, exact keywords are newly measurable, or ASIN history is short, also segment `0-30`, `31-60`, `61-90`, and `91-180 days`. Compare listings on age-appropriate launch velocity; do not impose a mature monthly-sales hurdle on products active for only days or weeks.

Measure, when fields permit:

- share of parents in each cohort;
- cohort sales share;
- cohort median sales and review count;
- proportion of new parents reaching practical milestones such as 200 or 500 monthly units;
- rising, flat and declining share among tracked ASINs;
- FBA versus FBM performance;
- dependence on low price, coupon or aggressive recent price cuts.

Do not compare a new product's missing pre-launch months with an older product's zero-sales months.

For emerging-product entry, also test:

- exact-search appearance and direction rather than broad-category traffic alone;
- whether several low-review ASINs convert, not just one head listing;
- whether later entrants reproduce early success;
- competitor-listing growth relative to demand growth;
- whether price, coupon or advertising deterioration signals a closing window;
- the opportunity cost of waiting versus a short, reversible third-round validation.

## 5. Keyword and traffic evidence

When keyword data is available, classify terms as exact purchase, use scenario, broad traffic or contamination before aggregation. Evaluate search volume, purchase volume/rate, PPC, title density, product count and click/conversion concentration when fields permit. Blank or unavailable values are unknown, not zero. Keyword totals confirm demand but are not additive with product sales or market-report totals.

Treat organic-traffic observations as a claim requiring evidence. Verify `3-5` relevant ASINs when possible using organic/paid share, organic keyword count, leading traffic terms and rank distribution. One ASIN with strong organic traffic proves that listing's success, not that demand is broadly distributable. User observations remain `用户线索/待验证` until supported by a workbook, screenshot or reproducible source.

## 6. Competition, quality and economics

Interpret low concentration in context. Fragmented sales plus rapid listing growth, generic branding, low ratings and falling prices often means copycat competition rather than a protected blue ocean.

Use a second-round veto check when:

- market or leading-product rating is below about `3.5`;
- most demand sits below roughly `$15` and FBA economics are unknown;
- a food-contact, heating, electrical, load-bearing, children or medical claim is central;
- demand is concentrated in one recent month;
- the apparent opportunity depends on one ASIN or one parent;
- estimated margins use incomparable FBM/FBA assumptions.

These are investigation triggers, not automatic universal eliminations.

Second-pass profitability is a veto screen, not a full profit model. Any residual after price, referral fee, FBA and target margin is a shared cost allowance for purchase, freight, duty, advertising, promotions, storage, returns and other costs. Do not label it profit. Use actual packaged logistics, supplier tiers and operating assumptions in third round.

## 7. SellerSprite-specific quality checks

- Treat literal placeholders or sentinels such as `136` in fields like Prime price, Q&A or shipping as missing unless the workbook proves otherwise.
- Do not interpret `Generic` as one consolidated brand moat; it may aggregate unrelated generic sellers.
- Check whether monthly sales are parent or child estimates before summing.
- Do not add market-report totals to competitor-report totals when their filters or ASIN universes differ.
- Use listing date and first nonblank history together; investigate large contradictions.
- Record the export date and treat the latest calendar month as partial when the export occurs before month end.

## 8. Confidence and decision logic

Assign confidence to the conclusion, not to the product:

- `高`: boundary is clean, key sources align, complete periods exist and major figures reconcile;
- `中`: direction is usable but one important source, period or scope check is limited;
- `低`: boundary, stability, sample coverage or economics could readily reverse the decision.

Use `观察/补数` only when the missing evidence is decision-changing. Otherwise complete the decision with a caveat.

Do not change a decision merely in response to user agreement or disagreement. When a decision changes, document the original basis, new or reinterpreted evidence, corrected assumption and why it crosses the decision boundary.

For every final recommendation, state:

1. what is verified;
2. what is inferred;
3. what remains missing;
4. what evidence would reverse the decision;
5. whether the direction should consume third-round research time.
