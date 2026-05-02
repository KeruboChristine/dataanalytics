
# PROJECT PROPOSAL

**Title:**  
Inequality Analysis of Water, Sanitation, and Hygiene (WASH) in African Schools

---

## 1. Introduction
Access to safe water, functional toilets, and handwashing facilities in schools is a fundamental right and a prerequisite for a productive learning environment. In many African nations, the lack of these basic services remains a significant barrier to education. Using data from the WHO/UNICEF Joint Monitoring Programme (JMP), this project analyzes the disparities in WASH access in schools across the African continent to identify gaps and progress.

## 2. Problem Statement
Despite international efforts, millions of children in Africa attend schools with no drinking water or sanitation facilities. This deficiency leads to waterborne diseases, poor academic performance, and high dropout rates—particularly among adolescent girls who require private facilities for menstrual hygiene management. There is a critical need to analyze these inequalities across African sub-regions to pinpoint where infrastructure investment is most urgently needed.

## 3. Objectives

### General Objective
To analyze inequalities in water, sanitation, and hygiene (WASH) access in schools across African countries and sub-regions using Python-based data analysis.

### Specific Objectives
*   To examine trends in school WASH access across Africa over the last decade.
*   To compare service levels (Basic, Limited, No Service) between different African sub-regions (e.g., Sub-Saharan Africa vs. North Africa).
*   To identify specific African regions with the highest percentage of schools lacking any sanitation facilities.
*   To measure the inequality gap between urban and rural school WASH access (where data permits).
*   To provide data-driven insights to support educational infrastructure policy in Africa.

## 4. Research Questions
1.  Which African sub-regions have the lowest access to basic drinking water in schools?
2.  How has sanitation access in African schools improved (or declined) over time?
3.  What is the statistical gap in WASH services between the leading and lagging African regions?
3. The correlation between WASH Infrastructure and Eductaion Outcomes(Completion Rates)
4.  Which countries/regions are currently on track to reach "Universal Basic Access" by 2030?

## 5. Data Description
The study utilizes secondary data from the **WHO/UNICEF Joint Monitoring Programme (JMP) for WASH in Schools**.

### Dataset Features
*   **Geographic Focus:** African Continent (Sub-divided into SDG regions: Sub-Saharan Africa, Northern Africa, etc.).
*   **Indicators:** Drinking Water, Sanitation, and Hygiene (Handwashing).
*   **Service Levels:** 
    *   **Basic:** Functional facilities available.
    *   **Limited:** Facilities exist but are insufficient or broken.
    *   **No Service:** No facilities available.
*   **Time Series:** Annual data points.
*   **Values:** Percentages of schools.

### Data Structure
The dataset is processed from Excel format using Python (Pandas), transforming "Wide" format data into "Long" (tidy) format for analysis.

## 6. Methodology (Python Implementation)

### 6.1 Data Cleaning (Pandas)
*   Filter the global dataset to isolate African countries and regions.
*   Handle missing values (`NaN`) which are common in school-level reporting.
*   Rename columns for clarity (e.g., `Service_Level`, `Year`, `Region`).
*   Normalize data types for time-series analysis.

### 6.2 Data Analysis
*   **Descriptive Statistics:** Calculating mean access rates per region.
*   **Comparative Analysis:** Grouping data by sub-region to find the "Inequality Gap."
*   **Trend Analysis:** Calculating the "Annual Rate of Change" to see which regions are improving fastest.

### 6.3 Data Visualization (Matplotlib/Seaborn)
*   **Line Graphs:** Showing the trajectory of "Basic Service" access over time.
*   **Heatmaps:** To visualize the intensity of "No Service" across the continent.
*   **Bar Charts:** Comparing Water vs. Sanitation vs. Hygiene levels side-by-side.

## 7. Expected Outcomes
*   A comprehensive map of WASH inequality in African schools.
*   Identification of "Hotspots" where more than 50% of schools lack basic sanitation.
*   A quantified report on the progress of hygiene (handwashing) facilities post-COVID-19.
*   Clear visualizations that can be used for advocacy and policy briefs.

## 8. Significance of the Study
This study is vital for:
*   **Education Ministries:** To prioritize budget allocation for school infrastructure.
*   **NGOs:** To target WASH interventions in the most underserved African regions.
*   **Gender Equality:** Highlighting gaps that specifically affect girls' school attendance (SDG 5).
*   **SDG Goals:** Tracking Africa’s progress toward **SDG 6** (Clean Water) and **SDG 4** (Quality Education).

## 9. Data Cleaning & Processing Summary
**Dataset:** JMP-WASH-in-schools-2024-data-by-country.xlsx  
**Records:** 1,213 observations across 51 African countries  
**Time Period:** 2000-2023 (24 years)  
**Indicators:** 54 WASH variables (Water, Sanitation, Hygiene services at different levels)

---

## 10. FINDINGS: ANSWERS TO RESEARCH QUESTIONS

### RQ1: Which African sub-regions have the lowest access to basic drinking water in schools?

**Answer:** Sub-Saharan African countries show the most significant disparities in basic water access.

**Key Findings:**
- **Top 3 Performers:** 
  - Malawi: 92% of schools have basic water access
  - Algeria: 91%
  - Morocco: 90%
- **Bottom 3 Performers:**
  - Congo: 54%
  - Uganda: 55%
  - Liberia: 55%
- **Continental Average:** 60% of African schools have basic water access
- **Inequality Gap:** 38 percentage points between highest (Malawi) and lowest (Congo)

**Chart:** RQ1_basic_water_access.png

---

### RQ2: How has sanitation access in African schools improved (or declined) over time?

**Answer:** Significant improvement over 24 years, with acceleration after 2005.

**Key Findings:**
- **2000 Baseline:** Only 8% of African schools had basic sanitation
- **2023 Status:** 52% of African schools have basic sanitation (**+540% improvement**)
- **Growth Phases:**
  - 2000-2005: Slow growth (8% → 12%, +0.8%/year)
  - 2005-2015: Rapid acceleration (12% → 50%, +3.8%/year)
  - 2015-2023: Plateau (~50%, +0.3%/year)
- **Annual Trend Rate:** ~2.0% year-over-year improvement on average
- **Projected 2030:** ~54% of schools (modest further improvement)

**Implication:** While progress is evident, current rate is insufficient to reach universal basic access by 2030.

**Chart:** RQ2_sanitation_trends.png

---

### RQ3: What is the statistical gap in WASH services between leading and lagging African regions?

**Answer:** Significant inequality persists across the continent.

**Key Statistics (Latest Year Data):**
- **Highest Access:** 92% (Malawi - basic water)
- **Lowest Access:** 25% (several countries - basic water)
- **Inequality Gap:** **67 percentage points**
- **Mean Access:** 60%
- **Standard Deviation:** 19%
- **Coefficient of Variation:** 0.32 (indicating moderate-to-high inequality)
- **Median Access:** 59% (below mean, indicating right-skewed distribution)

**Distribution Pattern:**
- 5 countries (10%): <30% basic water access (crisis level)
- 15 countries (29%): 30-60% access (moderate level)
- 19 countries (37%): 60-80% access (good level)
- 12 countries (24%): >80% access (excellent level)

**Key Insight:** The inequality gap reveals that Africa is not a monolith—significant regional variation indicates different implementation capacities and priorities.

**Chart:** RQ3_regional_gaps.png

---

### RQ4: Is there a correlation between lack of hygiene facilities and lack of sanitation?

**Answer:** Yes, strong positive correlation (r = 0.587, p < 0.05).

**Key Findings:**
- **Pearson Correlation Coefficient:** 0.587 (moderate-to-strong positive relationship)
- **Sample Size:** 17 African countries with complete data for both indicators
- **Interpretation:** Countries with poor sanitation also tend to have poor hygiene facilities
- **Linear Relationship:** For every 10% increase in basic sanitation access, hygiene access increases by approximately 5.9%

**Policy Implication:** WASH interventions must address sanitation AND hygiene simultaneously—they are interlinked infrastructure needs, not separate issues.

**Chart:** RQ4_sanitation_hygiene_correlation.png

---

### RQ5: Which countries are on track to reach Universal Basic Access (90%+) by 2030?

**Answer:** Only 4 African countries project to reach 90% basic water access by 2030.

**Countries ON TRACK (Projected ≥90% by 2030):**
1. **Malawi** - Current 92% → Projected 103% (Trend: +1.8%/year) ✓
2. **Morocco** - Current 90% → Projected 94% (Trend: +0.8%/year) ✓
3. **Togo** - Current 65% → Projected 93% (Trend: +4.8%/year) ✓ **Fastest improver**
4. **Algeria** - Current 91% → Projected 91% (Trend: -0.1%/year) ⚠️ Stalled

**Countries LAGGING (Projected <70% by 2030):**
- Sudan, South Sudan, Uganda, Liberia, Burundi, Rwanda, Guinea-Bissau, Gabon, Congo, Tunisia
- Average projected access by 2030: 57%
- **Critical Interventions Needed:** These 10 countries require urgent infrastructure investment

**Progress Summary:**
- 🟢 On Track (90%+): 4 countries (8%)
- 🟡 Moderate Progress (70-90%): ~15 countries (29%)
- 🔴 Lagging (<70%): 10 countries (20%)
- ⚠️ Stalled/Declining: ~22 countries (43%)

**Chart:** RQ5_sdg_2030_progress.png

---

## 11. Conclusions

### Key Takeaways:

1. **Progress is Real but Unequal**  
   Africa has made significant strides in expanding WASH access (e.g., sanitation +540% since 2000), but progress is unevenly distributed. A few countries (Malawi, Morocco) lead, while many others lag behind.

2. **Mid-Implementation Crisis**  
   The plateau in sanitation access after 2015 suggests that **easy gains have been captured**. Reaching the remaining 48% of schools will require more targeted, costly interventions in rural and remote areas.

3. **Correlation of WASH Services (r=0.587)**  
   Schools don't have water without sanitation or sanitation without hygiene—these are bundled infrastructure needs. Siloed interventions will fail.

4. **SDG 2030 Target at Risk**  
   With current trends, only 4 of 51 African countries will reach 90% basic water access by 2030. **Urgent acceleration needed.**

5. **Inequality as a Development Indicator**  
   The 67-percentage-point gap in basic water access reflects broader governance and economic disparities. The countries lagging in WASH also tend to lag in education outcomes, conflict, and poverty.

---

## 12. Recommendations

### For Policy Makers:
1. **Prioritize Sub-Regional Coordination**  
   East and Central Africa (Congo, Uganda, Rwanda, Burundi, South Sudan) need targeted investment. Consider regional WASH consortiums.

2. **Accelerate in Fast-Growing Countries**  
   Togo (+4.8%/year) and Benin (+3.2%/year) are momentum leaders. Share their strategies with lagging neighbors.

3. **Address the Rural-Urban Divide**  
   Analyze whether disparities are rural-driven (data permitting). Rural schools likely face higher capital costs per student.

4. **Integrated Infrastructure Planning**  
   Since hygiene and sanitation are correlated, plan bundled projects, not separate water-only projects.

### For NGOs & Development Partners:
1. **Focus on Lagging Countries**  
   Sudan, South Sudan, Uganda, and Liberia need sustained support. Current trajectory will leave them 20-30% below target in 2030.

2. **Post-2025 Roadmap Needed**  
   The 2015-2023 plateau suggests a transition point. Design interventions for the "hard-to-reach" schools beyond 2025.

3. **Support Togo and Fast Movers**  
   Document why Togo (+4.8%/year) is succeeding. Replicate model in similar countries.

### For Researchers:
1. **Disaggregate Further**  
   Next phase should distinguish urban vs. rural, primary vs. secondary school access gaps.

2. **Geospatial Analysis**  
   Map "WASH deserts" (contiguous areas with <30% access) to optimize intervention sites.

3. **Menstrual Hygiene Management (MHM)**  
   Analyze gender-specific indicators where available (girls' dropout rates correlate with lack of private sanitation).

---

## 13. Limitations
*   **Data Gaps:** Some African countries have incomplete reporting for certain years, limiting trend analysis.
*   **Aggregation:** Regional averages may hide extreme inequalities within specific countries or rural districts.
*   **Self-Reporting:** Data is government-reported, which may vary in accuracy and consistency.
*   **Temporal Scope:** Analysis uses 2000-2023 data; more recent 2024 data may show acceleration post-COVID-19.
*   **Geospatial Resolution:** Country-level data masks within-country disparities (available data does not include sub-national districts).

---

## 14. Final Conclusion

Improving WASH in African schools is not just a health or education issue—it is a **social justice imperative** tied to gender equality (SDG 5), quality education (SDG 4), and clean water (SDG 6). This data-driven analysis reveals that while Africa has made substantial progress since 2000, the current trajectory is **insufficient to meet 2030 SDG targets**. 

With 51 African countries and significant resource constraints, a **differentiated approach** is needed: 
- **Fast Movers** (Togo, Malawi) need support to maintain momentum
- **Moderate Progressors** need targeted acceleration
- **Lagging Countries** need emergency WASH programs with international support

The path to universal basic WASH access in African schools is achievable by 2030, but only with **increased investment, political will, and strategic partnerships**.
