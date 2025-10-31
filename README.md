# Germany-Energy-Time-Series-Exploratory-Data-Analysis
This project performs an Exploratory Data Analysis (EDA) on Germany's daily electricity consumption and renewable energy production (wind and solar) from 2006 to 2017. The goal is to identify and statistically verify key trends, seasonal patterns, and other properties within the time series data.

📊 Dataset
File: Germany_Energy_TimeSeries.csv

Content: Daily records of electricity consumption, wind power production, and solar power production.

Timespan: 2006-01-01 to 2017-12-31 (4383 entries).

Summary of Key Findings
This analysis successfully identified three distinct patterns in Germany's energy data: a long-term trend, a strong yearly seasonal cycle, and a clear weekly seasonal cycle.

1. Long-Term Trends (2006-2017)
Consumption: After an initial rise, there is a slight but consistent downward trend in median daily consumption from 2007 to 2017. The data also shows decreasing volatility in later years, suggesting consumption has become more stable and predictable.

Renewables: A strong, clear upward trend was found in both Wind and Solar power production, reflecting significant growth in renewable energy generation over the 12-year period.

2. Yearly Seasonality
Consumption: A strong yearly cycle is present, where consumption peaks in the cold winter months (December, January, February) and is lowest in the summer.

Renewables: Solar and Wind also show yearly seasonality.

Solar: Production is the inverse of consumption, peaking in the sunny summer months and dropping to near-zero in winter.

Wind: Production is higher and significantly more variable in the windier fall and winter months.

3. Weekly Seasonality
A clear and repeating weekly cycle was confirmed.

Consumption: Energy use is consistently high on weekdays (Monday-Friday) and drops noticeably every weekend (Saturday and Sunday).

⚙️ Analysis Methodology
The EDA was conducted using the following steps:

Data Loading and Inspection: The data was loaded from CSV, and its structure, data types, and null values were inspected.

Time Series Preprocessing: The 'Date' column was converted to a datetime object and set as the DataFrame's index. This step is crucial for enabling time-based slicing and analysis.

Feature Engineering: New columns ('Year', 'Month', 'Weekday Name') were extracted from the DatetimeIndex to allow for grouping and aggregation to analyze seasonal patterns.

Visualization & Pattern Analysis:

Line Plots: Plotted the full time series to visually identify long-term trends and yearly seasonality.

Zoomed-In Plots: Analyzed single years, months, and weeks to confirm the visual rhythm of both yearly and weekly cycles.

Boxplots: Used boxplots grouped by Month, Weekday, and Year to statistically confirm the seasonal patterns and trends identified in the line plots.

🛠️ Tools Used
Pandas

NumPy

Matplotlib

Seaborn
