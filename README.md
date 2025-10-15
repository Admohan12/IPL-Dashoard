# IPL-Dashoard
🏏 IPL Cricket Data Analysis Dashboard README
1. Project Overview
This repository features the Power BI file (IPL.pbix) for a detailed, interactive dashboard dedicated to analyzing Indian Premier League (IPL) cricket statistics. The dashboard provides comprehensive insights into various aspects of the tournament, including:

Team Performance: Evaluation of overall success, consistency, and rivalry results.

Player Analysis: Deep dive into batting and bowling metrics to identify top performers.

Match Dynamics: Analysis of factors like toss decisions, venue impact, and margin of victory.

The tool is designed for fans, sports analysts, and team management to quickly extract meaningful trends from the vast dataset.

2. Data Model & Source Files
The dashboard integrates data from multiple cleaned source files (which were part of your workflow) into a robust Star Schema model in Power BI.

Data Source (Conceptual)	Role in Model	Key Columns for Analysis
Historical Order Summary	Fact (Raw Material Orders)	Order made On, Supplier, Item
Supplier Details	Dimension	Supplier, Raw_Material, Supplier Rating
Raw Material Inventory	Fact (Inventory Snapshot)	Date, Raw_Material
Sales/Inventory Transactions	Fact (Sales/Consumption)	Date, Outlet_ID, Item_ID

Export to Sheets
Key Relationships for Filtering:
All major filtering across different fact tables is achieved through the use of shared Dimension Tables (e.g., a central Date Table is implicitly used to filter all time-based fact tables).

3. Key Dashboard Pages & Features
The report is structured into several pages for focused analysis:

A. Tournament Summary (Homepage)
KPIs: Total Runs, Total Wickets, Highest Team Score, Average Run Rate.

Visuals: Season-by-Season trend analysis for overall tournament scoring and team rankings by Win Percentage.

Interactivity: Primary slicers for Season and Tournament Stage (League/Playoffs/Final).

B. Player Performance Deep Dive
Batting Focus: View top batsmen ranked by Runs, Strike Rate, and Batting Average. Includes specialized metrics like Boundary Percentage (4s & 6s).

Bowling Focus: View leading bowlers ranked by Wickets, Economy Rate, and Bowling Average.

Insights: Use of dynamic measures to highlight Orange Cap and Purple Cap contenders for any selected season.

C. Venue & Match Dynamics
Venue Bias: Analysis showing which stadiums favor batting or bowling, often visualized through average scores and successful chase rates.

Toss Impact: Charts showing the percentage of matches won by the team that wins the toss and chooses to bat/bowl first.

Filters: Enables filtering by Venue and Innings Number (1st/2nd).

4. How to View and Use the Dashboard
Software Requirement: You must have Power BI Desktop installed on your machine.

File Access: Download the IPL.pbix file from this repository.

Open: Double-click the file to open it in Power BI Desktop.

Interaction: Use the visual slicers and filters present on the left side and top of each report page (e.g., selecting a Season or a specific Team) to apply filters across the entire report and explore the underlying statistics.

5. Technology Stack
Primary Tool: Microsoft Power BI Desktop

Data Sources: CSV/Excel files (Historical match data, player stats).

Language: DAX (Data Analysis Expressions) for creating advanced measures and KPIs.

Model: Star Schema / Dimensional Modeling.

