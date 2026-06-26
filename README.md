# Where Solar Meets Need: A County-Level Equity Analysis

Solar deployment across the U.S. has grown steadily over the past decade, but the communities carrying the highest energy costs have not been its primary beneficiaries. This project looks at where high energy burden and solar potential overlap at the county level, and whether the places that need it most are positioned to benefit.

*Lead analyst: Christian Dadzie | Environmental Data Science, Yale School of the Environment, Spring 2025*

---

![County Priority Classes Across the U.S.](images/County%20Priority%20Map.jpg)

*County priority classes across five states. Teal = highest need. Green = moderate. Gray = strongest technical opportunity.*

---

## The Question

Which U.S. counties face both high energy burden and meaningful solar potential, and are the people who need it most actually positioned to benefit?

## The Approach

Five datasets, two scales. Nationally, we plotted every U.S. state by energy burden vs. solar potential to find where the mismatch is largest. Five states landed in the high-burden, high-potential quadrant: **Michigan, Georgia, Pennsylvania, Ohio, and Indiana.** Florida, Texas, and California were excluded as outliers by land area.

We then ran a k-means cluster analysis on 489 counties across those five states, grouping them by solar potential, energy burden, BIPOC %, poverty rate, and per capita income. Three distinct profiles emerged. Beyond profiling the counties, we also tested whether those profiles follow a geographic pattern: whether high-need places tend to sit next to other high-need places, or whether the distribution is effectively random.

## What the Data Shows

**Priority 1 — Highest Need (102 counties)**
Average energy burden of 5% of income, BIPOC share of 43%, poverty rate of 25%, and per capita income of $19,585. Solar potential is lower here than in Priority 3, but these counties have the clearest case for targeted investment.

**Priority 2 — Moderate (282 counties)**
The dominant profile across Michigan, Ohio, Indiana, and Pennsylvania. Moderate burden (4.5%), lower BIPOC share (7%), income around $24,500.

**Priority 3 — Strongest Technical Opportunity (105 counties)**
Solar potential roughly 10x higher than Priority 1 counties, and the lowest energy burden (2.87%). Per capita income here averages $31,516, still well below the U.S. median of $42,220. The best technical conditions are not in the wealthiest places.

## Georgia Is a Story on Its Own

Georgia stands out immediately, nearly all teal on the map and an outlier among outliers. Of the 159 Georgia counties in this analysis, **97 are Priority 1**, more than Michigan, Ohio, Indiana, and Pennsylvania combined, which together total just 5. Older infrastructure, less efficient housing stock, and decades of underinvestment have compounded into a concentrated pattern that the statewide average does not capture.

## The Geography Is Not Random

It is not random. High-need counties cluster together, and the pattern holds consistently across the five states. This means the conditions driving energy inequity are not isolated to individual counties. They are shared across regions, shaped by the same underlying infrastructure gaps, economic histories, and policy environments. Broad statewide programs are likely to miss where need is most concentrated.

## What This Means

The highest solar potential and the highest energy burden do not sit in the same places. Any framework that prioritizes technical conditions alone will consistently favor counties that are already better off. The county-level picture also reveals concentration that disappears when data is aggregated to the state level, which has real implications for how programs like Justice40 and state solar block grants are designed.

---

## Data and Tools

Python, GeoPandas, scikit-learn (k-means), PySAL (Moran's I), Matplotlib

| Dataset | Source |
|---|---|
| Residential Solar Potential | NREL |
| Energy Burden | DOE LEAD Tool |
| Race, Poverty, Income | U.S. Census ACS |
| Health and Poverty | HDPulse |
| Shapefiles | U.S. Census TIGER/Line |
