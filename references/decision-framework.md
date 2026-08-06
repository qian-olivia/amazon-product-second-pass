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

## 4. New-product entry probability

Group listings by age:

- `0-3 months`: launch velocity only;
- `4-6 months`: early retention and post-launch decay;
- `over 6 months`: persistence and mature competition.

Measure, when fields permit:

- share of parents in each cohort;
- cohort sales share;
- cohort median sales and review count;
- proportion of new parents reaching practical milestones such as 200 or 500 monthly units;
- rising, flat and declining share among tracked ASINs;
- FBA versus FBM performance;
- dependence on low price, coupon or aggressive recent price cuts.

Do not compare a new product's missing pre-launch months with an older product's zero-sales months.

## 5. Competition, quality and economics

Interpret low concentration in context. Fragmented sales plus rapid listing growth, generic branding, low ratings and falling prices often means copycat competition rather than a protected blue ocean.

Use a second-round veto check when:

- market or leading-product rating is below about `3.5`;
- most demand sits below roughly `$15` and FBA economics are unknown;
- a food-contact, heating, electrical, load-bearing, children or medical claim is central;
- demand is concentrated in one recent month;
- the apparent opportunity depends on one ASIN or one parent;
- estimated margins use incomparable FBM/FBA assumptions.

These are investigation triggers, not automatic universal eliminations.

## 6. SellerSprite-specific quality checks

- Treat literal placeholders or sentinels such as `136` in fields like Prime price, Q&A or shipping as missing unless the workbook proves otherwise.
- Do not interpret `Generic` as one consolidated brand moat; it may aggregate unrelated generic sellers.
- Check whether monthly sales are parent or child estimates before summing.
- Do not add market-report totals to competitor-report totals when their filters or ASIN universes differ.
- Use listing date and first nonblank history together; investigate large contradictions.
- Record the export date and treat the latest calendar month as partial when the export occurs before month end.

## 7. Confidence and decision logic

Assign confidence to the conclusion, not to the product:

- `高`: boundary is clean, key sources align, complete periods exist and major figures reconcile;
- `中`: direction is usable but one important source, period or scope check is limited;
- `低`: boundary, stability, sample coverage or economics could readily reverse the decision.

Use `观察/补数` only when the missing evidence is decision-changing. Otherwise complete the decision with a caveat.

For every final recommendation, state:

1. what is verified;
2. what is inferred;
3. what remains missing;
4. what evidence would reverse the decision;
5. whether the direction should consume third-round research time.
