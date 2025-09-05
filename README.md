League of Legends Analytics Project 🎮📊

These past few weeks, I have been working on an analytics project focused on drawing insights from my League of Legends games. I enjoy playing ranked, but I am not always the best player. My goal with this project is to evaluate my performance, determine what I am doing well, and identify areas for improvement to increase my rank.

This project parses my past match history using the Riot API. Note that some aspects of the game—like items purchased, decision-making, or teammates’ performance—are not captured in my data.

You can follow along with my files in this repository.

Riot API Access 🛠️

To collect match history, I applied for an API key and used the following APIs:

Summoner V4: Retrieve a player's puuid from their summoner name.

Match V5 — puuid: Return a list of recent match IDs (up to 100).

Match V5 — matches: Return detailed match information in JSON format.

ETL Script: Python 🐍

The Python script extracts match data from Riot API, transforms it into a DataFrame, and loads it into MySQL Amazon RDS.

1. Import Libraries
   <img width="597" height="147" alt="image" src="https://github.com/user-attachments/assets/98b64b77-4209-4148-8825-17a5ad8ac11e" />
2. Initialize Variables
<img width="823" height="132" alt="image" src="https://github.com/user-attachments/assets/3fd5aeca-5bbe-467c-989b-d973b1f1579a" />
3. Function to Retrieve Match Stats
<img width="1127" height="1236" alt="image" src="https://github.com/user-attachments/assets/39f63ab6-f637-4b9e-b98b-5cac48213f39" />
Saving Data Locally 💾
<img width="728" height="363" alt="image" src="https://github.com/user-attachments/assets/e79b8f97-8acc-495f-b0c1-b8d43fdb8cb1" />
Power BI Dashboard 📊✨

After extracting and loading my match data into MySQL, I used Power BI Desktop to create an interactive dashboard. This helps visualize performance metrics and make data-driven decisions to improve ranked play.

Page 1: Overview ✅

This is the high-level strategic summary of my ranked performance.

Slicers (Filters):

Role Category: DPS / Utility

Champion Played: Searchable dropdown list

Date Range (Optional)

KPI Cards:

Total Games

Wins

Losses

Win Rate

Avg KDA

Win Rate by Role (Chart):

Clustered Column Chart

Axis: Role (Top, Jungle, Mid, ADC, etc.)

Value: Win Rate

Performance Over Time:

Line Chart

Axis: Date

Values: Win Rate, Avg KDA (secondary Y-axis optional)

Recent Matches Log:

Table visual

Columns: date_played, champion_played, Role, kills, deaths, assists, KDA, win

Page Layout :
<img width="1966" height="1169" alt="dashboard overview" src="https://github.com/user-attachments/assets/b79bd86f-3a6b-43ff-b38d-5f233b4e7ba9" />
Page 2: DPS Performance ⏳ (Future To-Do)

This page will focus on carry roles: Top, Mid, ADC.

Planned Features:

Page-level filter: Role Category = DPS

KPI Cards: Win Rate, Avg KDA, Avg DPM, Avg CSPM

Top DPS Champions: Clustered Bar Chart (champion_played vs Win Rate / Avg DPM)

DPS Analysis Scatter Chart:

X-Axis: Avg DPM (total_dmg / game_length)

Y-Axis: Avg CSPM (creep_score / game_length)

Color: Win/Loss

Tooltip: champion_played

Page 3: Utility Performance ⏳ (Future To-Do)

This page will focus on Jungle and Support roles, highlighting vision and assists.

Planned Features:

Page-level filter: Role Category = Utility

KPI Cards: Win Rate, Avg KDA, Avg Assists, Avg VSPM

Vision Score by Champion: Clustered Bar Chart (champion_played vs Avg VSPM)

Utility Role Comparison: Clustered Column Chart

Axis: Role (Jungle, Support)

Values: Avg VSPM, Avg Assists

This structure clearly shows what is complete (Page 1) and what’s planned (Pages 2 & 3).
