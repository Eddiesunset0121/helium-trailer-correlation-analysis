# Project 1: Helium Trailer Operational Efficiency : Linear Regression Analysis 

:large_blue_diamond: Project Objective:     
 - This project performs an in-depth analysis of operational data from a fleet of industrial gas trailers.
 - The primary goal is to understand the physical and operational factors that influence the fill volume of each trailer and to build a predictive 
   model for logistical planning.

(Please Note: The dataset used for this analysis is based on proprietary company information and cannot be shared publicly. This notebook is presented 
with all cell outputs pre-rendered to demonstrate the analytical workflow, key findings, and technical skills.)

:star2: Key Skills & Tools
- Data Cleaning & Manipulation: Pandas, NumPy
- Data Visualization: Matplotlib, Seaborn
- Statistical Modeling: Statsmodels (Ordinary Least Squares Regression)
- Core Competencies: Exploratory Data Analysis (EDA), Feature Engineering, Predictive Modeling, Model Diagnostics.

:herb: Analysis & Key Findings
The analysis was structured in three phases: EDA, correlation analysis, and predictive modeling.

:herb: Key Variable Relationships
- Pressure & Volume: A strong negative correlation exists between the pre-fill pressure and the volume of product that can be filled. This 
  confirms the physical principle that higher residual pressure limits fill capacity.
- Seasonal Temperature Effects: Both pre-fill and post-fill temperatures show a clear seasonal trend, indicating that ambient temperature is a 
  significant external variable impacting the process.

:herb: Predictive Model for Fill Volume
- An Ordinary Least Squares (OLS) linear regression model was built to predict volumn_filled based on pressure_prefill.
- The model demonstrates strong predictive power with an R-squared value of 0.914.
- The relationship is statistically significant, with the model providing the following predictive equation: volumn_filled = 2381.01 - (15.90 * pressure_prefill)

:herb: Model Validation
- The model's assumptions were validated using a residual plot and a Q-Q plot, both of which showed that the model is a good fit for the data.
  
:bulb: Business Application
This predictive model can be used by the logistics team to:
- Estimate the required fill volume for a trailer before it arrives at the plant.
- Optimize scheduling by prioritizing trailers with lower pre-fill pressures.
- Improve inventory management by more accurately forecasting product demand.
