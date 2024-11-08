# World_Electricity_Data_Analysis

# Overview
In this project, we analyzed electricity data for approximately 216 countries using data provided by the client. We began by extracting the data from the client’s database, which was in JSON format. The process involved transforming the JSON files into a long format, cleaning the data, filtering, and merging it with metadata. Finally, we saved the cleaned data into CSV files and used Power BI to generate valuable insights.

# Objectives
1) Trends in Electricity Generation by Source
2) Comparison Between Electricty Generation by Nuclear Source and Income Group
3) Least Electrified Countires
4) Electricity Loss Across Different Regions
5) Comparison between Electricity Access of Urban to the Rural region
   
# Tools used
1) Pandas library
2) JSON library
3) PowerBI Tool
# Methodology
Data Acquisition: The data was imported from the specified location.
Data Conversion: Initially in JSON format, the data was converted into a DataFrame. It was then melted to improve analysis and understanding, and finally saved in CSV format.
Data Cleaning: Using the Pandas library, the DataFrame was cleaned by removing duplicate values and unnecessary columns, as well as handling null and missing values.
Data Visualization: After cleaning, the data was loaded into Power BI to create visualizations and an interactive dashboard to uncover key insights.

# Summary
Load Metadata: The metadata file (Metadata.csv) is loaded into a DataFrame. This file contains additional information about countries, including Region and IncomeGroup.

Define File Mapping: A dictionary file_info maps each JSON file to its corresponding new column name and CSV output file name.

Load JSON Data: Each JSON file is read and converted into a DataFrame.

Clean DataFrame: The first row of each DataFrame, which contains header information, is removed. The remaining row is set as the new header. Reset the DataFrame index.

Melt DataFrame: The DataFrame is transformed from wide to long format using pd.melt(). The Year column is created, and the values are placed under a new column name as specified in file_info.

Remove Null Values: Rows with null values in the Year and values columns are removed. Year is converted to numeric and filtered to keep only years greater than 1999.

Merge Metadata: The Country Code from the melted DataFrame is used to merge with the metadata DataFrame, adding Region and IncomeGroup columns. Rows with null values in Region or IncomeGroup are removed.

Reorder Columns: The columns are reordered to place the value column at the end of the DataFrame.

Save to CSV: The cleaned and processed DataFrame is saved to a CSV file as specified in file_info.

Completion: A message is printed to indicate that data processing is complete and the individual CSV files have been created.

## Conclusion
Global Electrification:

Out of 216 countries analyzed, the world electrification rate stands at 80.71%.
Urban areas have significantly higher access to electricity (90.03%) compared to rural areas (76.23%).
Electricity Production by Source:

There has been a declining trend in electricity generation from oil and nuclear sources over the years.
Nuclear Energy Production:

High-income countries dominate nuclear energy production, contributing 74.71% of the total.
Upper-middle-income countries account for 16.83% of nuclear energy production.
Electricity Loss:

Sub-Saharan Africa experiences the highest electricity loss rate at 21.23%, indicating inefficiencies in the region's power distribution.
Electricity Access Disparities:

Significant gap in electricity access between urban and rural areas, especially in Sub-Saharan Africa, where rural access is only 28.65%.
Least Electrified Countries:

The least electrified countries are primarily located in Africa, with South Sudan having the lowest electrification rate at 3.68%.
Geographical Insights:

The world map highlights significant disparities in electricity access across different regions, with the highest access in North America and Europe and the lowest in Sub-Saharan Africa.
This analysis underscores the global disparities in electricity production and access, highlighting the need for targeted efforts to improve electrification, particularly in rural areas and lower-income regions.

Challenges Faced During The Project
Data Complexity:
Data Format and Structure: The initial data in JSON format is complex and nested, making it challenging to extract and convert into a usable DataFrame. Establishing a consistent structure during conversion is crucial.
Data Size: Handling and processing large datasets from 216 countries leads to performance issues and requires significant computational resources.

# Visualization:

Power BI experiences performance issues when dealing with large datasets, particularly when creating interactive dashboards. Optimization of the star schema and efficient data modeling are required to enhance performance.

Insight Generation: Generating actionable insights from the visualized data requires a deep understanding of the underlying patterns and potential socio-economic implications.
