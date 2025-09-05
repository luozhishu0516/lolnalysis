League of Legends Analytics Project 🎮📊

These past few weeks, I have been working on an analytics project focused on drawing insights from my League of Legends games. I enjoy playing ranked, but I am not always the best player. My goal with this project is to evaluate my performance, determine what I am doing well, and identify areas for improvement to increase my rank.

This project parses my past match history using the Riot API. Note that some aspects of the game—like items purchased, decision-making, or teammates’ performance—are not captured in my data.

League of Legends Analytics Project 🎮📊

These past few weeks, I’ve been working on an analytics project to draw insights from my League of Legends ranked games. My goal is to evaluate my performance, determine what I’m doing well, and identify areas for improvement to increase my rank.

⚠️ Note: Some aspects of the game—like items purchased, decision-making, or teammates’ performance—are not captured in this data.

1️⃣ Riot API Access 🛠️

To retrieve match history, I applied for a Riot API key and used three APIs:

Summoner V4: Retrieve puuid from the summoner name.

Match V5 — puuid: Get a list of recent match IDs (up to 100).

Match V5 — matches: Retrieve detailed match information in JSON format.

2️⃣ Python ETL Script 🐍

The Python script extracts match data from Riot API, transforms it into a DataFrame, and loads it into MySQL Amazon RDS.

   <img width="597" height="147" alt="image" src="https://github.com/user-attachments/assets/98b64b77-4209-4148-8825-17a5ad8ac11e" />
Variables & Setup

<img width="823" height="132" alt="image" src="https://github.com/user-attachments/assets/3fd5aeca-5bbe-467c-989b-d973b1f1579a" />

3️⃣ Save Data Locally 💾

<img width="1127" height="1236" alt="image" src="https://github.com/user-attachments/assets/39f63ab6-f637-4b9e-b98b-5cac48213f39" />


<img width="728" height="363" alt="image" src="https://github.com/user-attachments/assets/e79b8f97-8acc-495f-b0c1-b8d43fdb8cb1" />

Power BI Dashboard 📊✨

After extracting and loading my match data into MySQL, I used Power BI Desktop to create an interactive dashboard. This helps visualize performance metrics and make data-driven decisions to improve ranked play.

Page 1: Overview ✅

Slicers: Role Category, Champion Played, Date Range

KPI Cards: Total Games, Wins, Losses, Win Rate, Avg KDA

Win Rate by Role: Clustered Column Chart

Performance Over Time: Line Chart (Win Rate, Avg KDA)

Recent Matches Log: Table with date_played, champion_played, Role, kills, deaths, assists, KDA, win


<img width="1966" height="1169" alt="dashboard overview" src="https://github.com/user-attachments/assets/b79bd86f-3a6b-43ff-b38d-5f233b4e7ba9" />
Page 2: DPS Performance ⏳ (Future To-Do)

Page 2: DPS Performance ⏳ (Future To-Do)

Page-level filter: Role Category = DPS

KPI Cards: Win Rate, Avg KDA, Avg DPM, Avg CSPM

Top DPS Champions: Clustered Bar Chart

DPS Analysis Scatter Chart: Avg DPM vs Avg CSPM, colored by Win/Loss

Page 3: Utility Performance ⏳ (Future To-Do)

Page-level filter: Role Category = Utility

KPI Cards: Win Rate, Avg KDA, Avg Assists, Avg VSPM

Vision Score by Champion: Clustered Bar Chart

Utility Role Comparison: Clustered Column Chart (Jungle vs Support)

Insights & Takeaways 📝

Most successful champion: Sylas → Highest win rate, KDA, and kills

Creep score per minute below optimal → Need to farm minions more efficiently

Large champion pool → Should focus on mastering fewer champions

Dashboard allows for role-specific and champion-specific analysis

6️⃣ Skills Practiced 🛠️

Python: API calls, ETL, data manipulation

Riot API: Match data retrieval

AWS RDS & MySQL: Database creation and management

Power BI: Interactive dashboards and KPI visualization

7️⃣ Performance Report 📋

I created a detailed document summarizing my ranked performance between July 24, 2025 – September 4, 2025, analyzing 92 matches.

Can ve viewed in the pdf documents

Conclusion

You are a capable player with clear strengths on Sylas and Aurora. By improving farm efficiency, focusing on high-win champions, and making smarter in-game decisions, you can achieve a positive win rate and climb the ranked ladder.
