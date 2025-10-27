# Uncovering Global Development Patterns: A Clustering Approach to Aid Distribution for HELP International

## Project Overview
HELP International, a global NGO, aims to optimize how it allocates aid across countries. 
To ensure that assistance reaches the regions where it’s needed most, this project leverages unsupervised machine learning techniques,
specifically K-Means clustering and PCA to identify patterns among countries based on socio-economic and health indicators.
By grouping countries into distinct clusters, HELP International’s leadership can prioritize funding and tailor aid strategies according to development needs and similarities in national profiles.

## Objective
To categorize countries into development-based clusters using socio-economic indicators and uncover patterns that can guide strategic aid distribution for HELP International.

## Dataset Description
The dataset used for this analysis is `Country-data.csv`, containing 167 countries and 10 features capturing economic and health metrics.

- `country`: Name of the country  
- `child_mort`: Child mortality rate (per 1,000 live births)  
- `exports`: Exports as % of GDP  
- `health`: Government health spending as % of GDP  
- `imports`: Imports as % of GDP  
- `income`: Net per capita income (USD)  
- `inflation`: Annual inflation rate (%)  
- `life_expec`: Average life expectancy (years)  
- `total_fer`: Fertility rate (average births per woman)  
- `gdpp`: GDP per capita (USD)

## Project Workflow

### 1. Data Loading and Exploration
- Imported and inspected the dataset for structure, data types, and null values.  
- Verified there were no missing entries.

### 2. Categorical Encoding
Encoded the categorical `country` column using one-hot encoding to make it suitable for numerical modeling.

### 3. Feature Scaling
All numerical features were standardized using `StandardScaler` to ensure equal importance across features.

### 4. Dimensionality Reduction (PCA)
Applied PCA to reduce dimensionality after encoding.  
158 components captured 95% of the variance.

### 5. Clustering (K-Means)
Used the Elbow Method to determine the optimal number of clusters.  
K = 7 provided the best tradeoff between accuracy and interpretability.

### 6. Cluster Analysis
Each cluster represents a group of countries with similar development profiles.  
Cluster centers were analyzed to identify socio-economic trends and disparities.

## Insights
- Countries naturally grouped into clusters reflecting their economic and health status.  
- High-development clusters had high income, GDP, and life expectancy with low mortality rates.  
- Low-development clusters showed low income, high fertility, and high mortality rates.  
- Intermediate clusters represented transitioning economies.  
- Some outliers exhibited unique economic behaviors not fitting major groups.

## Tools Used
- Language: Python  
- Libraries: pandas, numpy, matplotlib, seaborn, plotly, scikit-learn, yellowbrick

## Conclusion
This project demonstrates how unsupervised learning can help organizations like HELP International identify development patterns and prioritize aid allocation effectively.  
The findings provide a data-driven basis for strategic humanitarian decision-making.
