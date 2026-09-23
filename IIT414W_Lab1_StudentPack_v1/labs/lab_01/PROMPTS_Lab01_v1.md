# Lab 1 · AI and contribution record

**Members:** TO COMPLETE.

---

## AI use

**AI used / not used:** AI used.

- **Tool:** Claude (Anthropic, Cowork desktop app)
- **Purpose:** orientation on the lab requirements, reviewing our notebook against the brief, and choosing and building the EDA questions.
- **Meaningful assistance:**
  - Flagged that our `dropna` on `qualifying_position` contradicted the brief.
  - Suggested the relevant columns for Q1 and Q3.
  - Provided working pandas/matplotlib code for Q3 (grid vs qualifying tables and chart).
- **How we used it:** we ran all code in the notebook and checked the outputs. What we accepted or changed is recorded per exchange below.

### Prompt log

| # | Prompt | AI output (summary) | Accepted / changed |
|:-:|---|---|---|
| 0 | *Orientation:* analyse the lab folder/MD files and give options for the three EDA questions | Flagged that the `dropna` in cell 6 contradicts the brief. It flips the training majority from **0** (600/1200, exact tie) to **1** (599/1197). Proposed EDA options A–F | TO COMPLETE |
| 1 | *"What columns in the dataset could we use to analyze this question?"* (Q1) | `qualifying_position`, `target_top10`, `season`/`round`, `qualifying_match`. Do not use `grid`, `position`, `points`, `status` or `laps` as predictors | TO COMPLETE |
| 2 | *"What columns in the dataset could we use to analyze this question?"* (Q3) | `qualifying_position`, `grid`, `target_top10`, `driver_id`/`season`/`round`, optional `status`. Hints: meaning of `grid = 0`, rows crossing the P10 cut, NaN qualifying rows | TO COMPLETE |
| 3 | *"How can I relate these two variables (grid and qualifying position), and which pandas commands should I use?"* | Full working code with `==`, `between()`, `pd.crosstab()` and `groupby().agg()`: mismatch summary, pit-lane starts, 2×2 table of P10 side, outcomes for rows crossing the cut | TO COMPLETE |
| 4 | *"How do I create a correlation chart at the end of Q3? Which of the data I already have should I cross?"* | Qualifying (x) vs grid (y). A first, more complex version was simplified at our request; **we used the simple scatter** (identity line, `alpha`, Pearson `.corr()`). Pointed out the misleading-correlation trap | TO COMPLETE |

---

## Decision and verification

**Own decision:** TO COMPLETE.

**Verification, observed result and limitation** *(notebook reference allowed)*: TO COMPLETE.

---

## Contributions

| Member | Contribution and evidence reference |
|---|---|
| TO COMPLETE | TO COMPLETE |
| TO COMPLETE | TO COMPLETE |