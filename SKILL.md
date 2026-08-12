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
5. Treat the user's target form, reference ASINs and differentiation plan as the decision object, not as a restriction on relevant evidence. Independently test the assumptions implied by that framing.
6. Decide the market boundary before choosing analytical layers. Analyze the exact market directly when it represents an independent purchase intent. Expand one layer outward only when broad keywords supply material traffic, substitutes divert demand, or the exact sample is too sparse; keep adjacent-market evidence separate and never add its totals to the exact market.

## Evidence independence

1. Record user observations and hypotheses as `用户线索/待验证` until a supplied workbook, screenshot or reproducible source supports them.
2. Do not change the analytical frame or decision merely because the user agrees, disagrees or proposes an interpretation. Reassess the evidence independently.
3. When the primary decision changes, state the original basis, the new or reinterpreted evidence, the corrected assumption and why the change is material.
4. Separate opportunity value from evidence confidence. Short history or a small sample lowers confidence; it does not automatically lower the opportunity or force `观察/补数`.

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
3. **Assess keyword evidence whenever keyword data is supplied.** Separate exact purchase terms, use-scenario terms, broad traffic terms and contaminated terms. Evaluate search volume, purchase volume/rate, PPC, title density, product count and click/conversion concentration when available. Treat missing values as unknown, never as zero, and use keyword evidence to confirm rather than add to product-market totals.
4. **Assess entry probability.** Use mature-market cohorts of `0-3 months`, `4-6 months`, and `over 6 months`. Switch to emerging-product cohorts of `0-30`, `31-60`, `61-90`, and `91-180 days` when exact keywords are newly appearing, most relevant listings are under six months old, or lifecycle coverage is short. Use age-appropriate milestones and never apply the same monthly-sales threshold to a listing active for days and one active for months.
5. **Assess emerging-product leading indicators.** Check whether exact search demand is appearing or growing, multiple low-review ASINs are converting, later entrants can reproduce early success, competitor supply is growing faster than demand, and the entry window is narrowing. Incorporate the cost of waiting for fast-copy standardized products; prefer a short named third-round veto check over passive multi-week observation when demand, price space and reversible execution permit it.
6. **Assess lifecycle evidence.** Use ASIN histories from each product's first active month. Compare the latest three complete months with the preceding baseline when history permits; otherwise limit the claim to launch velocity or early retention. Check peak dependence, volatility, survival, decline and price-sales dependence.
7. **Assess natural-traffic claims cautiously.** A single successful ASIN proves that listing, not distributable market demand. Prefer evidence across `3-5` relevant ASINs showing organic/paid traffic mix, organic keyword count, leading traffic terms and rank distribution. If those fields are absent, label the claim `缺失/待验证` even when the user reports it.
8. **Run veto checks.** Escalate quick checks when rating is abnormally low, price leaves little FBA room, the product makes food-contact/heating/load/electrical/children/medical claims, or one month dominates the trend. Detailed review mining, supplier validation, patent work and full profit modeling remain third-round tasks unless needed for a second-round veto.
9. **Reconcile sources.** Do not add or directly compare totals from workbooks with different filters, ASIN universes or date windows. Explain material conflicts and state which source controls each conclusion.
10. **Validate calculations and conclusions.** Recompute the highest-impact figures, inspect partial periods, parent duplication, null/zero treatment and scope coverage before reporting.

## Historical-data rules

- Exclude the current incomplete month and any other partial period from trend comparisons.
- Treat blank months before listing as `not yet listed`, not zero sales.
- Use the market-analysis trend for overall market history; use ASIN histories for cohort momentum and lifecycle. Current surviving ASINs cannot reconstruct the full past market because of survivorship bias.
- Treat short history as evidence with a narrower purpose: `0-3 months` supports launch-velocity judgment, `4-6 months` supports early retention, and longer history supports stability. Do not penalize a new ASIN merely for lacking old months.
- For emerging-product mode, match evidence to actual active days. Do not classify every `0-3 month` listing as a failed cohort or require mature-product milestones before it has had time to reach them.
- Flag possible ASIN repurposing or product replacement when old history conflicts with the current title, category, price or launch pattern.

## Economics boundary

- Use second-pass economics only as a veto screen. Calculate the cost allowance remaining after referral fee, FBA and an explicit target margin when inputs permit.
- Call the result a shared allowance for purchase cost, freight, duties, advertising, coupons, storage, returns and other costs; never call it profit.
- Reserve complete unit economics for third-round work using actual supplier tiers, packaged dimensions and weight, freight and duty, advertising conversion/CPC, promotions, returns and storage.

## Decision and report

Return exactly one primary decision:

- `进入第三轮`: evidence is sufficient and the opportunity survives second-round checks;
- `条件进入第三轮`: promising, but a named condition or veto check must pass;
- `观察/补数`: evidence is too unstable or a high-impact gap remains;
- `淘汰`: a supported market, quality, profit, compliance or structural veto is triggered.

Report the market boundary, available/missing sources, demand scale, demand stability, new-product entry chance, competition and price space, quality risk, simplified profit viability when available, data confidence, decision, and the smallest next data request. Separate confirmed evidence from inference and missing information.

Before finalizing, confirm that the report covers the exact market boundary, data quality, demand evidence, stability or emerging-product leading indicators, entry probability, concentration, keyword structure when supplied, price space, material gaps, confidence and exactly one decision. Add adjacent-market analysis only when it can materially change the exact-market decision.

Do not recommend ordering inventory from this pass.
