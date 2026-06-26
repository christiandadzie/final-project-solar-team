# Where Solar Meets Need: A County-Level Equity Analysis

The U.S. energy transition has a distribution problem. Low-income and majority-BIPOC communities spend the highest share of their income on energy, yet they have captured the least benefit from the solar boom. This project maps where those two realities collide and identifies which communities should be first in line for clean energy investment.

*Lead analyst: Christian Dadzie | Environmental Data Science, Yale School of the Environment - Spring 2025*

---

![County Priority Classes Across the U.S.](images/County%20Priority%20Map.jpg)

*County priority classes across five states. Teal = highest need. Green = moderate. Gray = strongest technical opportunity.*

---

## The Question

Which U.S. counties face both high energy burden and meaningful solar potential, and are the people who need it most actually positioned to benefit?

## The Approach

Five datasets, two scales. Nationally, we plotted every U.S. state by energy burden vs. solar potential to find where the mismatch is largest. Five states landed in the high-burden, high-potential quadrant: **Michigan, Georgia, Pennsylvania, Ohio, and Indiana.** Florida, Texas, and California were excluded as outliers by land area.

We then ran a k-means cluster analysis on 489 counties across those five states, grouping them by solar potential, energy burden, BIPOC %, poverty rate, and per capita income. Three distinct profiles emerged.

## What the Data Shows

**Priority 1 -- Highest Need (102 counties)**
Average energy burden: 5% of income. BIPOC share: 43%. Poverty rate: 25%. Per capita income: $19,585. Solar potential is lower here but not zero, and the combination of need and opportunity makes these the most important counties for equitable investment.

**Priority 2 -- Moderate (282 counties)**
Moderate burden (4.5%), lower BIPOC share (7%), income around $24,500. The dominant profile across Michigan, Ohio, Indiana, and Pennsylvania.

**Priority 3 -- Strongest Technical Opportunity (105 counties)**
Solar potential roughly 10x higher than Priority 1, and the lowest energy burden (2.87%). But even here, per capita income averages $31,516, well below the U.S. median of $42,220. The best technical conditions still sit in economically vulnerable places.

## Georgia Is a Story on Its Own

Georgia stands out immediately, nearly all teal on the map and an outlier among outliers. Of the 159 Georgia counties in this analysis, **97 are Priority 1**, more than Michigan, Ohio, Indiana, and Pennsylvania combined, which together total just 5. Older infrastructure, less efficient housing stock, and decades of underinvestment have compounded into a concentrated equity crisis. Whether this pattern overlaps with historically redlined areas is a question worth pursuing.

## The Geography Is Not Random

We tested whether counties with similar profiles cluster geographically or scatter randomly. **Moran's I = 0.62 (p = 0.001)**, a strong and statistically significant result. High-need counties neighbor other high-need counties. Broad statewide programs will miss the mark. The data supports regional targeting, focusing on clusters of adjacent counties rather than one-off interventions.

## What This Means for Investment and Policy

Two things are clear. First, chasing the best technical conditions is the wrong default: the counties with the highest solar potential are not the ones most in need. Equity-first targeting means weighting financial stress and socioeconomic vulnerability alongside megawatts. Second, state-level averages hide more than they reveal. A state can look moderate overall while containing pockets of severe inequity at the county level. Programs like Justice40 and state block grants should be designed around the county-level reality, not the state average.

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
