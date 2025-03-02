# Insurance-Market-Segmentation
The project talks about data-driven insurance market segmentation using K-Prototypes clustering to optimize underwriting and risk management in Panama City.


## Background and Overview

The Florida residential insurance market, particularly in Panama City, faces immense strain due to the increasing frequency of natural disasters such as hurricanes and flooding. Despite homeowners paying some of the highest premiums in the U.S., insurers struggle with unsustainable claim costs, leading to market instability and reduced options for risk management.

This project, a Drexel LeBow Capstone Project in collaboration with Precisely, aims to introduce a data-driven segmentation approach using K-Prototypes clustering. The goal is to help insurers optimize underwriting, refine pricing strategies, and enhance risk management.

## Data Structure Overview

The dataset used for this analysis was obtained through Precisely API queries, consisting of:-

Property Attributes: Size, year built, roof type, exterior walls, floor type

Demographics: Age group, income group, property tenure

Flood Risk Factors: Flood zone, elevation, 100-year flood zone distance

Coastal Risk Factors: Distance to the nearest coast


Data Cleaning & Preprocessing:-

Consolidated datasets from multiple CSV files (address fabrics, demographic data, property attributes, flood risk, coastal risk)

Removed duplicate records and handled missing values

Standardized data formats and validated consistency

Identified key predictive variables using Random Forest feature selection


## Executive Summary

To tackle the issue of rising insurance costs and risk mismanagement, we applied K-Prototypes Clustering to segment properties into four distinct clusters. This method allowed us to analyze both numerical and categorical features, making it more effective than traditional segmentation approaches like ZIP-code-based premium calculations.

Key Findings:

Cluster 1: High-risk, small, modern properties near flood-prone areas

Cluster 2: High-risk, large, modern properties with older populations

Cluster 3: Moderately high flood risk, older and smaller properties

Cluster 4: Moderate flood risk, newer and mid-sized properties

Our model provides insurers with a strategic framework to optimize pricing, adjust premiums, and manage risk exposure effectively.

##  Insights Deep Dive

### Key Feature Selection:
Using Random Forest and Gradient Boosting Models, we identified the top seven most influential factors affecting insurance premiums:

Property Living Square Footage

Elevation

Distance to Nearest Coast

Property Year Built

100-Year Flood Zone Distance

Age Group

Property Tenure

These factors were used as inputs for the K-Prototypes clustering model to segment the market effectively.
![image](https://github.com/user-attachments/assets/55acab6a-dce9-4aa0-93b0-170d09a6a047)

### Flood Risk Score Development:
We created a Flood Risk Score by combining Elevation and Distance to Flood Zone, weighted based on their feature importance from the Random Forest Model:

Elevation (Weight: 0.55)

Distance to Flood Zone (Weight: 0.45)

This score provided a more granular assessment of flood risk beyond traditional FEMA flood zone classifications, making risk evaluation more precise and actionable.

![image](https://github.com/user-attachments/assets/eb5a21c5-a633-4dbc-8e3a-17a3c3b53439)


### Clustering Methodology & Model Selection:
Why K-Prototypes?

Unlike K-Means (for numerical data) or K-Modes (for categorical data), K-Prototypes efficiently handles mixed data types.

It allowed us to incorporate both numerical features (e.g., square footage, elevation) and categorical features (e.g., age group).

Optimal Cluster Selection:

We applied the Elbow Method, identifying 4 as the optimal number of clusters for the segmentation.

### Results of Clusters
The segmentation results indicate that Clusters 1 and 2 pose the highest financial risk to insurers, necessitating higher premiums and strict underwriting measures. In contrast, Cluster 4 presents a significant business opportunity due to lower flood risk and a younger demographic.

![image](https://github.com/user-attachments/assets/ad804bec-6202-490c-96cc-d76e80d4557f)



## Recommendations

### For Insurance Companies:
Increase premiums for Clusters 1 & 2 to reflect their high risk and claim potential.

Offer discounts for flood-mitigation efforts in Cluster 3, incentivizing property owners to invest in risk-reducing measures.

Expand coverage in Cluster 4 with competitive pricing, targeting lower-risk customers.

Implement risk-adjusted deductibles, increasing them for high-risk clusters while keeping them lower for moderate-risk properties

### Strategic Business Actions:
Encourage policyholders in high-risk clusters to adopt flood-proofing measures by offering premium incentives.

Diversify insurer portfolios by reducing exposure to Clusters 1 & 2 while expanding in moderate-risk areas.

Reassess underwriting policies to incorporate more granular risk factors, such as historical claims data.

Develop bundled insurance products that offer incentives for combining home, flood, and hurricane coverage, improving customer retention.

## Learnings and Challenges

### Challenges Faced:
The dataset was highly complex, with inconsistencies in property attributes and missing values that required extensive cleaning and imputation.

Handling mixed data types for clustering was a challenge, necessitating advanced techniques such as K-Prototypes rather than traditional K-Means clustering.

### Industry Learnings:
Insurance pricing models often over-rely on ZIP codes, which do not accurately capture flood risk at the property level.

Demographic factors, such as age and homeownership tenure, significantly influence insurance claims frequency and premium adjustments.

### Areas for Improvement:
More granular flood risk indicators, such as historical claims data and property elevation maps, could improve segmentation accuracy.

Future iterations could incorporate real-time climate change projections to assess evolving flood risk trends.

### Key Takeaways:
Data-driven segmentation improves risk assessment and pricing fairness.

Insurers can optimize profitability by tailoring policies to cluster-specific risk profiles.

Incorporating non-traditional factors like elevation and flood proximity can enhance premium modeling.
