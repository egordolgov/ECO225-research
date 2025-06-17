# Do Social Media Discussions about Government Spending Affect Consumer Confidence?

This repository contains the paper, code, data, and documentation for a two-part analysis exploring whether real-time Twitter discourse around government spending during the 2020 U.S. election season is associated with shifts in U.S. consumer confidence. 

## Table of Contents

- [Overview](#overview)  
- [Data](#data)  
- [Methodology](#methodology)   
- [Key Findings](#key-findings)   

## Overview

We combine three datasets:

1. **Twitter data** (Jan–Nov 2020) filtered for fiscal-policy keywords  
2. **University of Michigan Consumer Sentiment Index** (CSI) for Oct–Dec 2020  
3. **Median household income by state** (2020)  

Our analysis proceeds in two stages:

- **Project One (Exploratory Analysis):**  
  - Summary statistics on tweet volume, engagement, and sentiment  
  - Time-series plots aligning tweet activity with CSI movements  
  - Choropleth maps of regional sentiment and confidence  

- **Project Two (Econometric Modeling):**  
  - OLS regressions linking tweet features (volume, sentiment, engagement, political affiliation) to CSI  
  - Interpretation of key coefficients in economic context  
  - Geospatial plots and dual-axis visualizations  

## Data

- **Raw tweets**  
  - JSON/CSV of tweets containing keywords like “stimulus,” “relief package,” etc.  
  - Fields: text, timestamp, geolocation, sentiment, likes, retweets, replies  

- **Consumer Sentiment Index (CSI)**  
  - Monthly CSI values from the University of Michigan (Oct–Dec 2020)  

- **Household Income**  
  - 2020 median household income by U.S. state  

## Methodology

1. **Preprocessing & Merging**  
   - Clean and filter tweets  
   - Compute sentiment scores (–1 to +1)  
   - Aggregate by date and state  
   - Join with CSI and income data  

2. **Exploratory Analysis**  
   - Summary tables of volume and sentiment  
   - Bar charts, line graphs, scatterplots, and choropleth maps  

3. **Regression Modeling**  
   - OLS regressions of CSI on:  
     - Tweet volume  
     - Average sentiment score  
     - Engagement metrics (likes, retweets)  
     - Political-affiliation indicators  
   - Controls: median income, state fixed effects  
   - Interpretation of coefficients and fit statistics  

## Key Findings

### Exploratory Analysis
- Tweet sentiment and volume both show positive correlation with month-to-month CSI changes.  
- Regions with higher average sentiment often report higher CSI.

### Econometric Modeling
- A one-unit rise in average tweet sentiment is associated with a statistically significant increase in CSI.  
- Engagement (likes, retweets) exhibits diminishing returns.  
- Political-affiliation of tweets (e.g., Trump-tagged) adds explanatory power beyond pure sentiment.


