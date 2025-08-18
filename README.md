# Housing Price Analysis in Poland (2018–2024)

## Project Overview
This project analyzes housing price dynamics in 17 major Polish cities between 2018 and 2024.  
The dataset was cleaned and normalized, then explored with:
- **Time series clustering** (DTW + TimeSeriesKMeans),
- **Breakpoint detection** (PELT),
- **Visualization of trends and structural changes**.

The goal was to identify major turning points in the housing market and group cities with similar price dynamics.


## Technologies
- Python 3.x
- Pandas, NumPy
- Matplotlib, Seaborn
- tslearn (DTW, TimeSeriesKMeans)
- ruptures (PELT)


## Data
- Source: **National Bank of Poland (NBP)**, quarterly transaction prices of apartments.  
- Period: **Q1 2018 – Q4 2024**  
- Cities: 17 largest Polish cities (e.g., Warsaw, Kraków, Gdańsk, Wrocław).


## Methods

### 1. Clustering (TimeSeriesKMeans + DTW)
- Compared cities based on similarity of housing price trajectories.  
- Optimal number of clusters determined using **silhouette score**.  
- Results:  
  - For the full period: best fit with `k = 2–3`,  
  - For sub-periods: e.g., in “Period II” the best fit was `k = 3`.

### 2. Breakpoint Detection (PELT)
- Detected statistically significant turning points in housing price dynamics.  
- Key breakpoints identified:  
  - **Q1 2019** – end of cheap credit phase, faster growth,  
  - **Q3 2021** – pre-adjustments before interest rate hikes,  
  - **Q4 2021** – start of interest rate hikes,  
  - **Q4 2022** – slowdown due to war, inflation, and reduced mortgage activity.


## Insights
- **Housing prices in Poland rose continuously between 2018–2021**, with sharp acceleration during the COVID-19 pandemic.  
- **Detected breakpoints** align with macroeconomic and geopolitical events:  
  - Interest rate hikes in 2021,  
  - War in Ukraine and inflation shock in 2022.  
- **Cities can be clustered** into groups with similar price dynamics, which can support forecasting and housing policy design.

