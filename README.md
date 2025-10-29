Clean Energy Investment Opportunity Analysis

View the notebook: https://colab.research.google.com/drive/1OLOlevyQ9hNgWlFU1BTO0oi04BcddiDX?usp=sharing

⚠️ Disclaimer
This is a data analysis learning project using publicly available Kaggle datasets. The data may contain inaccuracies and should NOT be used for actual investment decisions. This project demonstrates Python skills and analytical thinking only.

📊 Project Overview
A Python-based exploratory data analysis (EDA) project examining renewable energy capacity, population, and investment trends across multiple countries. The goal is to practice data manipulation, custom metric creation, and visualization techniques while exploring patterns in the clean energy sector.
Learning Focus: Applying Python data science tools to real-world datasets and developing frameworks for multi-dimensional analysis.

🎯 Analysis Objectives
•	Practice calculating growth metrics (CAGR) from time-series data
•	Develop custom scoring systems combining multiple variables
•	Compare trends across different categories (countries, energy types)
•	Create clear visualizations to communicate data insights
•	Build reusable functions for metric calculations

🛠️ Technical Skills Demonstrated
Tools & Libraries:
•	Python 3.x
•	pandas (data manipulation)
•	numpy (numerical operations)
•	matplotlib (data visualization)
•	Google Colab environment

Key Functions Built:
# Calculate Capacity Per Capita
market_saturation['Capacity Per Capita (MW/person)'] = (
    market_saturation['Installed Capacity (MW)'] / 
    market_saturation['Population']
)
# Normalize CAGR (0 to 1 scale)
investment_analysis['CAGR_norm'] = (
    (investment_analysis['CAGR (%)'] - investment_analysis['CAGR (%)'].min()) /
    (investment_analysis['CAGR (%)'].max() - investment_analysis['CAGR (%)'].min())
)
# Formula: 60% weight on CAGR growth, 40% weight on low saturation (room to grow)
investment_analysis['Investment Opportunity Score'] = (
    0.6 * investment_analysis['CAGR_norm'] + 
    0.4 * (1 - investment_analysis['Saturation_norm'])
)
Analysis Techniques:
•	Multi-year trend analysis
•	Cross-category comparisons
•	Custom metric development
•	Data ranking and filtering
•	Visual storytelling through charts

💡 Skills & Concepts Applied
Skill Area	What I Practiced
Data Cleaning	Handling missing values, data type conversions, filtering
Feature Engineering	Creating calculated columns (CAGR, saturation metrics)
Aggregation	Grouping data by country and energy type
Visualization	Bar charts, scatter plots, comparative analysis
Business Logic	Translating domain knowledge into scoring formulas

📈 Analysis Approach
Metrics Developed:
1.	CAGR (Compound Annual Growth Rate)
o	Measures growth momentum over time period
o	Formula-based calculation practice
2.	Market Saturation Index
o	Ratio of capacity to population
o	Normalization and scaling practice
3.	Opportunity Score (Custom Composite Metric)
o	Combines growth and saturation
o	Demonstrates multi-factor analysis
Outputs Created:
•	Comparative rankings across countries
•	Energy type trend comparisons
•	Scatter plot analysis of growth vs. saturation
•	Top N filtering and presentation

👤 About
Nils Liu
MBA, MSc Candidate | Learning Data Analytics
📍 San Francisco Bay Area
🔗 www.linkedin.com/in/nils-chen-yu-liu
Building data analysis skills through hands-on projects.

📝 How to Use This Project
1.	View the notebook: Click "Open in Colab" badge above
2.	Download data: Get the dataset from Kaggle
3.	Run analysis: Execute cells sequentially
4.	Experiment: Modify metrics and create your own insights

📄 Data Source
Dataset: Global Renewable Energy and Indicators Dataset from Kaggle
Link: https://www.kaggle.com/datasets/anishvijay/global-renewable-energy-and-indicators-dataset?resource=download
Note: Data accuracy not verified. Used for educational purposes only.
