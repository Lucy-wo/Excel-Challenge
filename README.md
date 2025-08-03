# Kickstarter Campaigns — Excel Analysis

## Summary
An Excel-based analysis of Kickstarter campaigns using **pivot tables** and **pivot charts** to understand success rates by **category**, **sub-category**, **time (month/year)**, and **goal size**. Headline findings:
- Overall success rate ≈ **53%**; **Music** leads with **~77%** success, followed by **Theater** at **~60%**. Together they account for ~2,093 projects (about half of all records). 
- Within Music, several **sub-categories reached 100% success** (e.g., classical, pop). 
- **Seasonality**: volume peaks **May–July** (380+ projects/month); **Mar–Apr** show the **best success rate (~60%)** and **lowest failure (~32%)**, while **Sep–Oct** perform worst; **Dec** has more failed than successful projects. 
- **Higher funding goals** correlate with **lower success** and **higher failure**. 

---

## Goal
Provide clear, decision-ready insights for creators and platforms on **when** to launch, **where** to focus (categories/sub-categories), and **how** goal size relates to outcomes—using only Excel so stakeholders can **replicate and explore** without code.

---

## Procedure
1. **Data Intake**
   - Import the Kickstarter dataset into Excel; standardize fields (state, category, sub-category, goal, dates).
2. **Feature Prep**
   - Derive **Year/Month** from launch dates; bucket **goal ranges** (e.g., <$1k, $1–5k, $5–10k, …).
3. **Exploratory Pivots**
   - Pivot 1: **Category × State** (success/failed/canceled counts & rates).
   - Pivot 2: **Sub-Category × State** to surface high/low performers.
   - Pivot 3: **Month × State** (across years) to measure seasonality.
   - Pivot 4: **Goal Range × State** to evaluate goal–success relationship.
4. **Visualization**
   - Pivot charts + slicers for interactive filtering by year, country, and category.
5. **Quality Checks**
   - Validate totals vs. raw; spot anomalies and duplicates.

---

## Results
- **Best categories:** Music (~77% success) and Theater (~60%). 
- **Sub-category winners:** Several music sub-genres hit **100% success** in this sample. 
- **Timing matters:** Highest volume May–July; strongest outcomes Mar–Apr; weakest Sep–Oct; December skews to failures. 
- **Goal sizing:** Larger goals tend to underperform (lower success, higher failure). 

---

## Business Impact
- **Creators:**  
  - Launch in **Mar–Apr** when possible and consider **Music/Theater** opportunities if relevant.  
  - **Right-size funding goals** to improve odds of success.
- **Platforms/Advisors:**  
  - Tailor guidance and **goal recommendations** by category and season.  
  - Use seasonal insights for **marketing calendars** and **spotlight campaigns** with higher probability of success.

---

## Next Steps to Make It Better
1. **Normalize campaign duration**  
   Projects vary from <10 to ~90 days; standardize or control for duration in rate comparisons. 
2. **Add geography detail**  
   City-level data would enable more granular regional insights (currently limited). 
3. **Audit data coverage**  
   Resolve discrepancy between instructions and observed success share (~50% met goal in raw). 
4. **Deeper goal analysis**  
   Model probability of success vs. **continuous goal** (log scale) and category interactions.
5. **Cohort/seasonality controls**  
   Compare months **within each year** to separate seasonality from macro trends.
6. **Automate dashboards**  
   Build an Excel dashboard with slicers (year, country, category, goal range) or port to Power BI/Tableau.

---

## How to Reproduce (Excel)
1. Open the raw dataset in Excel.
2. Insert **Pivot Tables** for the views above; add **calculated fields** for success rates.
3. Create **Pivot Charts** and add **slicers** (Year, Category, Country, Goal Range).
4. Save charts to a summary sheet for stakeholders.
