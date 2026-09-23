# Lab 1 · AI and contribution record

**Members:** 
- Andy Villarroel
- Agustín Reyes

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
| 0 | *Orientation:* analyse the lab folder/MD files and give options for the three EDA questions | Flagged that the `dropna` in cell 6 contradicts the brief. It flips the training majority from **0** (600/1200, exact tie) to **1** (599/1197). Proposed EDA options A–F | Accepted |
| 1 | *"What columns in the dataset could we use to analyze this question?"* (Q1) | `qualifying_position`, `target_top10`, `season`/`round`, `qualifying_match`. Do not use `grid`, `position`, `points`, `status` or `laps` as predictors | Accepted |
| 2 | *"What columns in the dataset could we use to analyze this question?"* (Q3) | `qualifying_position`, `grid`, `target_top10`, `driver_id`/`season`/`round`, optional `status`. Hints: meaning of `grid = 0`, rows crossing the P10 cut, NaN qualifying rows | Accepted |
| 3 | *"How can I relate these two variables (grid and qualifying position), and which pandas commands should I use?"* | Full working code with `==`, `between()`, `pd.crosstab()` and `groupby().agg()`: mismatch summary, pit-lane starts, 2×2 table of P10 side, outcomes for rows crossing the cut | Accepted |
| 4 | *"How do I create a correlation chart at the end of Q3? Which of the data I already have should I cross?"* | Qualifying (x) vs grid (y). A first, more complex version was simplified at our request; **we used the simple scatter** (identity line, `alpha`, Pearson `.corr()`). Pointed out the misleading-correlation trap | Accepted |
| 5 | *"What columns should I use for EDA question 2?"* | Suggested `qualifying_position` to identify missing values and `target_top10` to compare final outcomes. Also recommended reporting row counts and group sizes because only a few rows have missing qualifying positions | Accepted |
| 6 | *"How can I get the percentage of null values in each column?"* | Suggested `train.isna().mean().mul(100)` to calculate the percentage of missing values in each column, together with `train.isna().sum()` to report null counts | Accepted |
| 7 | *"Is there a better graph for EDA question 2?"* | The top-10-rate graph compares rows with qualifying information against only 3 rows without it, so it is potentially misleading and does not directly answer whether dropping missing rows changes the training majority. A better graph would compare class counts before and after removing missing qualifying rows. The rate graph can remain as a secondary observation, but the majority comparison should support the main conclusion | Accepted |

---

## Decision and verification

**Own decision:** 
- **EDA question 1:** How well does qualifying position anticipate a top-ten finish?
- **EDA question 2:** Does the training majority change if rows with missing qualifying positions are dropped?
- **EDA question 3:** Are Grid and Qualifying position the same number? Do they match?
- We decided to use only the training data for EDA and to report both observed values and limitations.
- We also decided to keep rows with missing qualifying positions and use the training-majority fallback rather than dropping them.
- What was not directly asked in the prompts was the final wording of the EDA questions, the interpretation of the results, the final data-handling decision, and the limitations of the small missing-value group. These were our own decisions based on the notebook outputs.


**Verification, observed result and limitation** *(notebook reference allowed)*: 
- **Q1:** The selected columns and analysis were based on prompt 1. The results and interpretation were checked by running the train-only analysis in the notebook.
- **Q2:** Prompts 5–7 guided the choice of `qualifying_position`, `target_top10`, null percentages, and the graph. The full training data contained 1,200 rows with 600 class-0 and 600 class-1 outcomes, so the tie-breaking majority was class 0. After removing the 3 rows with missing qualifying positions, the remaining 1,197 rows contained 598 class-0 and 599 class-1 outcomes, changing the majority to class 1. The limitation is that only 3 rows were removed.
- **Q3:** Prompts 2–4 guided the use of `qualifying_position`, `grid`, and `target_top10`, including the comparison tables and scatter plot. The outputs were checked by running the notebook cells. The analysis is observational and does not establish causation.
---

## Contributions

| Member | Contribution and evidence reference |
|---|---|
| Andy Villarroel | EDA Question 1,3 for evidence there are the commits made in github |
| Agustín Reyes | EDA Question 2, prompts made for the team, for evidence there are the commits in github |