# Insurance-Market-Segmentation
This repository talks about data-driven insurance market segmentation using K-Prototypes clustering to optimize underwriting and risk management in Panama City.


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
