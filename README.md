# IBM-Data-Science-Specialization

# Winning the Space Race with Data Science: Predicting Falcon 9 Landing Success

## Project Overview
This project leverages data science methodologies to predict the success of SpaceX's Falcon 9 first-stage landings. By analyzing historical launch data, the project aims to optimize cost estimations for future launches, providing actionable insights into the factors influencing landing outcomes.

---

## Table of Contents
1. [Executive Summary](#executive-summary)  
2. [Introduction](#introduction)  
3. [Methodology](#methodology)  
4. [Results](#results)  
5. [Conclusion](#conclusion)  
6. [Appendix](#appendix)  

---

## Executive Summary
### Key Objectives
- Predict Falcon 9 first-stage landing success using historical launch data.  
- Identify factors (e.g., payload mass, launch site, orbit type) correlated with landing outcomes.  

### Findings
- **Accuracy**: Predictive models achieved **83.33% accuracy**, with Logistic Regression and KNN performing optimally.  
- **Trends**: Success rates improved over time, peaking in 2017, with certain orbits (e.g., GEO, ES-L1) showing 100% success.  
- **Payload Impact**: Heavy payloads (>10,000 kg) in LEO/ISS orbits had higher success rates.  

---

## Introduction
### Problem Statement
SpaceX’s competitive advantage lies in reusable rockets. Accurately predicting first-stage landing success enables better resource allocation and cost savings.  

### Key Question  
*Can historical launch data determine if the Falcon 9’s first stage will land successfully?*  

### Significance  
- **Cost Reduction**: Reusability cuts launch costs by ~30%.  
- **Data-Driven Decisions**: Insights guide mission planning and booster design.  

---

## Methodology
### Data Collection
- **Sources**:  
  - **SpaceX API**: Rocket specs, launch sites, payload data (JSON format).  
  - **Wikipedia**: Historical launch records (HTML tables).  
- **Tools**: Python (`requests`, `BeautifulSoup`, `pandas`).  

### Data Wrangling & EDA
- **Cleaning**: Labeled outcomes as `1` (success) or `0` (failure).  
- **Visualization**:  
  - Flight number vs. payload mass.  
  - Launch site success rates (e.g., KSC LC-39A: 76.7%).  
- **SQL Queries**: Identified unique launch sites, NASA’s total payload (45,596 kg), and first successful ground landing (2015-12-22).  

### Interactive Analytics
- **Folium Maps**: Geospatial analysis of launch sites.  
- **Plotly Dash Dashboard**:  
  - Success rates by site/orbit.  
  - Payload vs. success correlation.  

### Predictive Analysis
- **Models Tested**: Logistic Regression, SVM, Decision Tree, KNN.  
- **Performance**:  
  | Model          | Accuracy | F1-Score |  
  |----------------|----------|----------|  
  | Logistic Reg.  | 86.67%   | 90.91%   |  
  | Decision Tree  | 91.11%   | 93.75%   |  

---

## Results
### Key Insights
1. **Flight Number vs. Success**: Higher flight numbers (recent launches) correlate with improved success.  
2. **Orbit Types**: ES-L1, GEO, and HEO orbits had 100% success rates.  
3. **Payload Mass**:  
   - Failures were common with payloads <10,000 kg.  
   - Heavy payloads in LEO/ISS orbits succeeded consistently.  

### Visual Highlights  
- **Folium Map**: Proximity to coastlines/highways influenced success ratios.  
- **Dashboard**: KSC LC-39A had the highest success rate (76.7%).  

---

## Conclusion
### Recommendations
- **Model Selection**: Use Logistic Regression/KNN for balance of speed and accuracy.  
- **Future Work**: Incorporate weather/seasonal data to enhance predictions.  

### Impact  
Predictive insights can reduce SpaceX’s operational costs by optimizing launch strategies.  

---

## Appendix
### Repository  
- **GitHub**: [IBM-Data-Science-Specialization](https://github.com/DebarjunChakraborty/IBM-Data-Science-Specialization.git)  
- **Tools**: Python, SQL, Folium, Plotly Dash.  

### Data Sources  
- SpaceX API: [API Documentation](https://docs.spacexdata.com)  
- Wikipedia: [Falcon 9 Launch Log](https://en.wikipedia.org/wiki/List_of_Falcon_9_and_Falcon_Heavy_launches)  

---

## Acknowledgements  
- **IBM Skills Network** for project guidance.  
- **SpaceX** for providing open-access launch data.  
