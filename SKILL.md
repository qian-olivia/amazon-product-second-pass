---
name: amazon-product-second-pass
description: "Analyze SellerSprite or similar Amazon niche-market, competitor, and ASIN history Excel exports to complete a second-pass product-direction screening. Use when the user provides any subset of market analysis, competitor listings, historical monthly sales/revenue/price, first-pass shortlist, screenshots, or related evidence and wants a decision on whether a precise niche should enter deeper third-round research. Treat the three core workbooks as recommended rather than mandatory: identify missing evidence, explain its decision impact, request only high-value additions, and continue after user confirmation with explicit confidence and warning labels."
---

# Amazon product second pass

Evaluate one exact product direction at a time and decide whether it deserves third-round work. Treat the result as a research-prioritization decision, never as inventory-order approval.

## Required companion skills

Use `spreadsheets:Spreadsheets` to inspect Excel files. For quantitative recommendations, use `data-analytics:analyze-data-quality`, `data-analytics:product-business-analysis`, and `data-analytics:validate-data`; use `data-analytics:build-report` when a durable report is appropriate.

Read `references/decision-framework.md` completely before analyzing the supplied data.

## Intake and source recognition

1. Inventory every supplied file and identify its role from sheet names and columns, not only its filename:
   - market analysis: market overview, industry sales/search trend, concentration, price, rating, listing-age and seller distributions;
   - competitor detail: one row per ASIN with current sales, price, reviews, rating, fulfillment, listing date, category and packaging data;
   - ASIN history: monthly sales, revenue or price columns by ASIN;
   - optional evidence: first-pass/manual shortlist, keyword data, review exports, screenshots, supplier cost, FBA inputs, patent or compliance evidence.
2. Confirm the analysis unit: one precise niche defined primarily by title-indicated core function and purchase intent, with product form, installation and use scenario as secondary boundaries.
3. Preserve the original Amazon/SellerSprite subcategory as evidence. Do not merge different purchase markets merely because their category labels overlap, and do not split a genuine keyword-defined niche solely because Amazon placed its listings in several subcategories.
4. Deduplicate current-product comparisons by parent ASIN when possible. Retain child-level history only when variation behavior matters.

## Missing-evidence protocol

The market, competitor and history workbooks are recommended, not startup requirements.

1. Analyze the files already available before asking for more.
2. Request additional data only when it could materially change the decision. Name no more than three high-value requests at once and state:
   - exact data or export needed;
   - question it would answer;
   - bias or uncertainty if unavailable.
3. When a core source is missing, present a short warning and ask whether to continue only if the missing source materially changes the analytical frame. If the user has already instructed or confirmed continuation despite gaps, do not ask again.
4. After confirmation, complete the analysis with available evidence. Never invent missing metrics or silently substitute a weaker source.
5. Label each important statement as `已验证事实`, `分析推断`, or `缺失/待验证`, and lower the overall confidence accordingly.

## Analysis workflow

1. **Validate the market boundary.** Measure relevant-ASIN share, parent coverage, mixed-product contamination and category dispersion. Split the direction if titles reveal different core functions or purchase purposes.
2. **Assess current demand and structure.** Use market scale, complete-period sales/search trends, medians and distributions, CR1/CR3/CR10, price bands, rating bands, listing-age mix and seller/fulfillment structure.
3. **Assess entry probability.** Compare established listings with cohorts aged `0-3 months`, `4-6 months`, and `over 6 months`. Evaluate how many new parents reach meaningful sales, whether momentum survives beyond launch, and whether success depends on extreme discounting.
4. **Assess lifecycle evidence.** Use ASIN histories from each product's first active month. Compare the latest three complete months with the preceding baseline; check peak dependence, volatility, survival, decline and price-sales dependence.
5. **Run veto checks.** Escalate quick checks when rating is abnormally low, price leaves little FBA room, the product makes food-contact/heating/load/electrical/children/medical claims, or one month dominates the trend. Detailed review mining, keyword strategy, supplier validation, patent work and full profit modeling remain third-round tasks unless needed for a second-round veto.
6. **Reconcile sources.** Do not add or directly compare totals from workbooks with different filters, ASIN universes or date windows. Explain material conflicts and state which source controls each conclusion.
7. **Validate calculations and conclusions.** Recompute the highest-impact figures, inspect partial periods, parent duplication, null/zero treatment and scope coverage before reporting.

## Historical-data rules

- Exclude the current incomplete month and any other partial period from trend comparisons.
- Treat blank months before listing as `not yet listed`, not zero sales.
- Use the market-analysis trend for overall market history; use ASIN histories for cohort momentum and lifecycle. Current surviving ASINs cannot reconstruct the full past market because of survivorship bias.
- Treat short history as evidence with a narrower purpose: `0-3 months` supports launch-velocity judgment, `4-6 months` supports early retention, and longer history supports stability. Do not penalize a new ASIN merely for lacking old months.
- Flag possible ASIN repurposing or product replacement when old history conflicts with the current title, category, price or launch pattern.

## Decision and report

Return exactly one primary decision:

- `进入第三轮`: evidence is sufficient and the opportunity survives second-round checks;
- `条件进入第三轮`: promising, but a named condition or veto check must pass;
- `观察/补数`: evidence is too unstable or a high-impact gap remains;
- `淘汰`: a supported market, quality, profit, compliance or structural veto is triggered.

Report the market boundary, available/missing sources, demand scale, demand stability, new-product entry chance, competition and price space, quality risk, simplified profit viability when available, data confidence, decision, and the smallest next data request. Separate confirmed evidence from inference and missing information.

Do not recommend ordering inventory from this pass.
