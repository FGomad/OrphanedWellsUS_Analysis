# Orphaned Wells USA — Data Analysis & Geospatial Visualization

Exploring the environmental burden of ~100,000 abandoned oil & gas wells across the U.S. through data cleaning, analysis, and interactive geospatial visualization.

---

## About

Orphaned wells are oil and gas wells abandoned without proper closure, where no legally responsible operator can be found. Often drilled decades ago, these wells were left behind by companies that went bankrupt or ceased operations. They pose serious risks including methane leaks and groundwater contamination, public safety hazards from unstable well sites, and a growing financial burden on state and federal agencies responsible for cleanup.

This project uses real data from the **U.S. Environmental Protection Agency (EPA)** to clean, analyze, and visualize orphaned well records — making the scale of this problem visible and accessible.

---

## Dataset

| Detail | Info |
|---|---|
| **Source** | U.S. Environmental Protection Agency (EPA) |
| **Records** | ~100,000 wells |
| **Key Fields** | State, County, Latitude, Longitude, Status |
| **Output** | `cleaned_orphaned_wells.csv` |

---

## Data Cleaning

The raw EPA dataset contained over **40+ inconsistent status labels** (e.g., "PA", "P&A", "WO", "Orphaned Well", "Abandoned, Unknown Location"). These were standardized into **9 clear categories**:

| Category | Examples of Raw Values |
|---|---|
| PLUGGED | PA, P&A, XX |
| ORPHANED | OR, Orphaned, Forfeited |
| ABANDONED | AB, Abandoned Well |
| TEMP_ABANDONED | TA, Idle, SI |
| ACTIVE | Active, AL, HP |
| WORKOVER | WO |
| CANCELLED | Canceled, DA, DM |
| RECLAMATION | Environmental Reclamation |
| UNKNOWN | Unknown, UN |

Additional cleaning steps included removing records with missing coordinates, converting all text fields to uppercase, and standardizing column names to lowercase with underscores.

---

## Key Findings

### 1. Most Wells Are Orphaned
The majority of wells in the dataset are classified as **Orphaned** — meaning no operator is responsible for plugging or remediating them. Only a small fraction have been properly **Plugged**.
![Well Status Distribution](https://github.com/FGomad/OrphanedWellsUS_Analysis/blob/main/Orphaned%20Well%20Project/Figures/distribution%20of%20doc%20orphan%20well%20status.png)

### 2. Hotspots in Appalachia and Texas
The geospatial map reveals **dense clusters** of orphaned wells in the **Appalachian Basin** (Pennsylvania, West Virginia, Ohio) and across **Texas**. These regions reflect a long history of oil and gas drilling and represent high-priority zones for environmental remediation.
![Geospatial Map](https://github.com/FGomad/OrphanedWellsUS_Analysis/blob/main/Orphaned%20Well%20Project/Figures/geospatial_distribution.png)

### 3. The Cleanup Gap
The data shows a significant gap between the number of orphaned wells and the number that have been plugged, highlighting the scale of the challenge facing regulators and communities.
![Orphaned vs Abandoned Ratio](https://github.com/FGomad/OrphanedWellsUS_Analysis/blob/main/Orphaned%20Well%20Project/Figures/orphaned_vs_abandoned_ratio.png)

### 4. Estimated Plugging Cost by State
The cost of plugging orphaned wells varies significantly across states. This visualization highlights the estimated financial burden each state faces, reinforcing the need for targeted federal funding and prioritized remediation efforts.
![Cost Estimation by State](https://github.com/FGomad/OrphanedWellsUS_Analysis/blob/main/Orphaned%20Well%20Project/Figures/cost_estimation_by_state.png)

## Tech Stack

`Python` · `pandas` · `Plotly Express` · `Matplotlib` · `Jupyter Notebook`

## Author

**FGomad** — [GitHub Profile](https://github.com/FGomad)

---

## License

Open source — feel free to use, share, and build upon this work.

