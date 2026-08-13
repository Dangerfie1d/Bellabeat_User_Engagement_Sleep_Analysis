# Bellabeat_User_Engagement_Sleep_Analysis
Bellabeat manufactures high-tech, health-focused smart products. This project analyzes time-series heart rate and sleep tracking data to evaluate device wear-consistency during overnight hours and formulate targeted digital marketing strategies to boost product engagement, feature adoption, and retention.

Bellabeat Consumer Smart Device Usage Analysis
Executive Summary: An end-to-end data analysis analyzing non-Bellabeat smart device tracking data to identify consumer activity and sleep consistency habits. The insights guide high-level marketing strategies for Bellabeat wellness devices, focusing on gamification, habit formation, and nighttime wearability.

Business Problem & Context
Background: Bellabeat is a high-tech manufacturer of health-focused smart products for women, including the Bellabeat app, Leaf tracker, Time watch, and Spring smart water bottle.

Core Objective: Analyze non-Bellabeat smart device fitness data to uncover consumer usage trends, patterns, and behaviors. Use these insights to recommend strategic digital marketing and product engagement initiatives for Bellabeat products.

Key Stakeholders: Urška Sršen (Cofounder & Chief Creative Officer), Sando Mur (Cofounder & Executive Team Member), and the Bellabeat Marketing Analytics Team.

Key Business Insights & Impact
Overnight Tracking Gap: Analysis of heart rate and sleep patterns revealed that users frequently remove their devices overnight or fail to record continuous overnight tracking, leading to missing data gaps.

Engagement & Usage Disparity: High-engagement users who consistently track activity and overnight sleep patterns maintain stronger long-term device habits than non-consistent users.

Strategic Growth Opportunity: Addressing device comfort and battery recharge timing during non-sleep hours can significantly increase overnight wearability, unlocking continuous health monitoring benefits.

Data & Methodology
Data Sources
FitBit Fitness Tracker Data: Public dataset (CC0) containing tracker data from Fitbit users, including heart rate, physical activity, and sleep monitoring outputs.

heartrate_seconds_merged & Daily Activity Tables: Cleaned dataset containing timestamped heart rate and activity records.

Analytical Approach
Data Cleaning & Wrangling: Processed and cleaned datasets using Python (Pandas) to handle date/time formatting, separate timestamps, and address null/missing values.

Database Management & SQL Querying: Created an SQLite database (Bellabeat_user_database.db) combining all activity and heart rate tables. Executed aggregation queries to calculate daily user tracking intervals, sleep activity, and heart rate trends.

Behavioral Analysis: Analyzed heart rate data patterns (specifically between typical sleep hours of 11 PM – 6 AM) to assess device wear consistency.
SQL
Query example used to extract peak daily heart rate timestamps per user
SELECT 
    Id AS user_id,
    DATE(Time) AS hr_date,
    MAX(Time) AS last_hr_time
FROM heartrate_seconds_merged
GROUP BY Id, DATE(datetime(Time))
ORDER BY user_id, hr_date;

Figure 1: SQL Query execution in DB Browser for SQLite showing date/time extraction and daily heart rate aggregation across users.

Strategic Recommendations & Action Plan

1. Promote Nighttime Wearability & Comfort (Product Marketing):
   Action: Position Bellabeat devices (e.g., Leaf or Time) as lightweight, stylish, and comfortable alternatives designed specifically for non-intrusive overnight sleep and heart rate tracking.
   Target Metric: Increase overnight wear consistency across active users.

2. Gamification & Streak Incentives (Bellabeat App):
   Action: Implement streak badges and push notifications celebrating continuous daily and overnight tracking milestones to strengthen user commitment.
   Target Metric: Improve 30-day user retention and daily sync rates.

3. Smart Charging & Routine Reminders (Digital Campaigns):
   Action: Educate users through targeted in-app messages and digital campaigns on optimal device charging routines (e.g., charging during morning showers rather than overnight).

Stack & Tools
Data Processing & Automation: Python (Pandas)[cite: 3]
Database & Querying: SQL (SQLite / DB Browser for SQLite)
Documentation & Reporting: Markdown, Pages/Text Documents

Repository Structure
data/                    # Cleaned FitBit CSV datasets
sql/                     # SQL scripts for table aggregation and time-series extraction
python/                  # Python scripts for data cleaning and SQLite DB creation
database/                # Bellabeat_user_database.db
reports/                 # Case study report summary and findings
 README.md                # Project documentation

Christopher David Dangerfield
LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
Email: [your.email@example.com](mailto:your.email@example.com)
