
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
4.  Is there a correlation between lack of hygiene facilities (handwashing) and lack of sanitation in schools?
5.  Which countries/regions are currently on track to reach "Universal Basic Access" by 2030?

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

## 9. Limitations
*   **Data Gaps:** Some African countries may have incomplete reporting for certain years.
*   **Aggregation:** Regional averages may hide extreme inequalities within specific countries or rural districts.
*   **Self-Reporting:** Data is often based on government-reported school censuses which may vary in accuracy.

## 10. Conclusion
Improving WASH in African schools is not just a health issue, but a critical educational and economic necessity. This Python analysis will provide the empirical evidence needed to understand the scale of inequality and advocate for a future where every African child attends a school with safe water and dignified sanitation.




