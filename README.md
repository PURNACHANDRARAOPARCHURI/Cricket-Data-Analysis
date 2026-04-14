# 🏏 IPL Data Analysis Dashboard (2008–2025)

## 📊 Project Overview

This project is an interactive **Power BI dashboard** that analyzes Indian Premier League (IPL) data from **2008 to 2025**.
It provides insights into team performance, player statistics, and season-wise outcomes.

---

## 🚀 Features

### 🏆 Season Insights

* Champion (Winner of final match)
* Runner-up
* Season filter (dynamic)

### 📈 Team Performance (Points Table)

* Matches Played
* Wins
* Losses
* Tie Matches
* No Result
* Points Calculation
* Ranking (based on points)

### 🔥 Player Statistics

* Top Run Scorer (Orange Cap)
* Top Wicket Taker (Purple Cap)
* Most 6’s hitter
* Most 4’s hitter

### 📊 Overall Metrics

* Total Matches
* Total 4’s
* Total 6’s
* Total Teams
* Total Venues
* Total Centuries & Half-centuries

---

## 🧠 Key Logic Implemented

### 🏆 Champion Calculation

* Determined using **last match date of the season**
* Winner of that match = Champion

### 📊 Points Table Logic

* Win → 2 points
* Tie → 1 point
* No Result → 1 point
* Loss calculated as:

  ```
  Losses = Matches Played - Wins - Tie - No Result
  ```

### 🔗 Data Modeling

* Relationships:

  * `team1 → teams_data` (Active)
  * `team2 → teams_data` (Inactive, handled using USERELATIONSHIP)
* Measures handle both team1 & team2 participation

---

## 🗂️ Dataset Used

* `ipl_matches_data` → Match-level data
* `ball_by_ball_data` → Ball-by-ball stats
* `players_data` → Player details
* `teams_data` → Team information

---

## 🛠️ Tools & Technologies

* Power BI
* DAX (Data Analysis Expressions)
* Power Query (Data Transformation)

---

## ⚠️ Challenges Faced

* Handling **inactive relationships (team2)**
* Correctly calculating:

  * Wins / Losses
  * Tie matches
* Removing teams not present in selected season
* Identifying champion without explicit "Final" column

---

## ✅ Solutions Implemented

* Used `USERELATIONSHIP()` for team2
* Used `FILTER()` for accurate row-level logic
* Created `Show Team` filter to remove inactive teams
* Used `MAX(date)` to identify final match

---

## 📌 Future Improvements

* Add Net Run Rate (NRR)
* Highlight top 4 teams (playoffs)
* Add match-level drill-through
* Enhance UI with animations and tooltips

---

## 📷 Dashboard Preview

*(Add screenshots here)*

---

## 👤 Author

**Purna Chandra Rao**

---

## ⭐ If you like this project

Give it a ⭐ and share your feedback!
