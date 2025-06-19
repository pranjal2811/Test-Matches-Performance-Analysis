# Test-Matches-Performance-Analysis
Hello folks! My name is Pranjal Joshi, and I am delighted to present my project on Business Analytics. This project involved a comprehensive analysis of cricket match data, providing valuable insights into overall team and individual player performance.

# Project Overview
The core of this project was to perform an in-depth analysis of cricket match data. The primary goal was to understand various aspects of cricket performance, including overall team statistics, detailed batting performance, and in-depth bowling analyses. The dataset provided a rich source of information for descriptive statistics, trend analysis, and identifying top performers.

# Objectives
The project was structured around several key objectives, divided into different levels of complexity:

Data Overview
Understand the dataset structure, including the number of entries, columns, and data types from Batting_Stats and Bowling_Stats.
Identify key performance indicators (KPIs) for overall, batting, and bowling performance.
Overall Performance Analysis
Visualize total runs by team.
Analyze the average bowling economy trend over time.
Display total wickets taken by team.
Detailed Batting Statistics
Identify the highest run-scorer.
Visualize batsmen with the highest and lowest strike rates.
Present top and bottom performers based on runs scored.
In-Depth Bowling Analysis
Identify the leading wicket-taker.
Visualize total wickets taken by individual bowlers.
Display total runs given by individual bowlers.
# Implementation Steps
I utilized Power BI Desktop for data loading, manipulation (including Power Query for custom columns and DAX for measures), and dashboard visualization.

Data Loading and Initial Inspection.

Loaded Batting_Stats and Bowling_Stats tables into Power BI.
Inspected the tables to understand their structure and content, noting the available columns like Balls, Batsman, Fours, Inning, Match_Date, Series (in Batting_Stats) and bowler, economy, inning, maiden, Match_Date, noball, over, runs, series, wickets, wide (in Bowling_Stats).
Identified the overall KPIs from the dashboard's Over All Perfomance tab: Total Match (25), Total Runs (24254), Avg Strike Rate (50.48), Total Sixes (307), Total Fours (2740), Total Wickets (856).
Custom Column Creation.

In Power Query, for both Batting_Stats and Bowling_Stats tables, I added 4 new columns each by using "Add Column" from "Text" transformations, specifically leveraging the Series column. While the exact transformations varied based on parsing the Series string (e.g., "New Zealand vs Australia, 2nd Test at Christchurch, Mar 08 2024, Australia tour of New Zealand"), these columns were designed to extract:
Match Type (e.g., "Test", "ODI", "T20")
Opponent Team (e.g., "Australia", "England")
Match Number (e.g., "1st", "2nd")
Host Nation/Location Type (e.g., "New Zealand", "India")
Custom Measure Creation. 

Team = LEFT(Batting_Stats[inning], FIND(" ", Batting_Stats[inning]) - 1): This DAX measure was created in the Batting_Stats table to extract the team name from the inning column. For example, from "Australia Batting", it extracts "Australia".
Team = LEFT(Bowling_Stats[inning], FIND(" ", Bowling_Stats[inning]) - 1): Similarly, this DAX measure was created in the Bowling_Stats table to extract the team name from its inning column.
Overall Performance Analysis

Visualized total runs per team using a bar chart (Overall Runs By Team).
Presented the average bowling economy trend over time using a line chart (Avg Bowling Economy Economy Trend).
Displayed total wickets by team using a bar chart (Overall Wickets By Team).
Implemented filters for Series, Inning, and Team to allow dynamic viewing.
Detailed Batting Statistics 

Highlighted the Highest Run Scorer as Yashasvi Jaiswal.
Displayed Highest Strike Rate by Batsman and Lowest Strike Rate by Batsman using line charts.
Utilized bar charts for Top Performers and Bottom Performers based on runs.
Included filters for Team Comparison, Match Date, Batsman, and Series.
In-Depth Bowling Analysis

Identified Leading Wicket Taker as Pat Cummins.
Presented Total Wickets By Bowler and Total Runs Given By Bowler using bar charts.
Included a detailed table displaying bowler, sum of wickets, and sum of runs.
Provided filters for Inning, Team Comparison, Match Date, Series, and Bowler.
# Results and Conclusion
The analysis provided a clear picture of cricket performance based on the given dataset:

Overall Performance: The dashboard summarizes key metrics like total matches played (25), total runs (24254), and total wickets (856), offering a quick overview of the analyzed period.
Team Performance: Visualizations clearly show which teams performed best in terms of runs scored and wickets taken, with Australia consistently ranking high across various metrics.
Batting Insights: The dashboard identifies top batsmen like Yashasvi Jaiswal as the highest run-scorer and highlights trends in strike rates.
Bowling Insights: Pat Cummins is clearly identified as the leading wicket-taker, and insights into individual bowler performance in terms of wickets and runs conceded are provided.
Data Enhancement: The creation of 8 new columns via Power Query from the Series column significantly enhanced the data's analytical granularity, allowing for more specific filtering (e.g., by Match Type or Opponent).
Dynamic Team Extraction: The two DAX measures for Team extraction from the inning column proved invaluable for consistent team-based filtering and analysis across all visuals.
Trends: The Avg Bowling Economy Trend visualization provides a time-series view of bowling efficiency, showing a general improvement (decrease in economy) over the period.
This project provided valuable experience in data cleaning, data transformation using Power Query, DAX measure creation, exploratory data analysis, visualization, and interpreting statistical results within the domain of sports analytics.

# Tools and Technologies Used
Power BI Desktop: Core tool for dashboard development, data modeling, and visualization.
Power Query: Used for data extraction, transformation, and loading (ETL), specifically for creating custom columns.
DAX (Data Analysis Expressions): Utilized for creating calculated columns and measures to derive new insights from the data.
# Contact Information
Name: Pranjal Joshi
GitHub: https://github.com/pranjal2811
LinkedIn: https://www.linkedin.com/in/pranjaljoshi2811
Email: pranjaljoshi2811@gmail.com
