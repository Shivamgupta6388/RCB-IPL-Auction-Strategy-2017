<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=CC0000,FFD700&height=200&section=header&text=RCB%20IPL%20Auction%20Strategy&fontSize=40&fontColor=fff&animation=fadeIn&fontAlignY=35&desc=Data-Driven%20Player%20Selection%20for%202017%20Mega%20Auction&descAlignY=55&descSize=16" width="100%"/>

# 🏏 IPL Data Analysis — Royal Challengers Bangalore
### Auction Strategy 2017 | SQL + Data Analytics Project

[![Author](https://img.shields.io/badge/Author-Shivam%20Gupta-CC0000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Shivamgupta6388)
[![Institute](https://img.shields.io/badge/Institute-Newton%20School-FFD700?style=for-the-badge)](https://newtonschool.co)
[![SQL](https://img.shields.io/badge/SQL-MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Status](https://img.shields.io/badge/Status-Completed-00C853?style=for-the-badge)](/)
[![Repo](https://img.shields.io/badge/GitHub-RCB--IPL--Strategy-181717?style=for-the-badge&logo=github)](https://github.com/Shivamgupta6388/RCB-IPL-Auction-Strategy-2017)

</div>

---

## 🎯 Problem Statement

> *"RCB has reached the IPL final in 2009, 2011, and 2016 — and lost all three."*

As a **Sports Data Analyst hired by RCB**, the mission was clear:

- Analyse **9 seasons of IPL data** (2008–2016)
- Identify **top-performing players** using on-field statistics
- Build a **data-backed auction strategy** for the 2017 Mega Auction
- Optimise for **performance + value for money**

---

## 📦 Dataset Overview

| Metric | Value |
|--------|-------|
| 📋 Total Tables | 18 |
| 👤 Players | 469 |
| 🏟️ Matches | 255 |
| 📅 Seasons | 9 (2008–2016) |
| 🎯 Ball-by-Ball Records | 37,284+ |
| 🏟️ Venues | 35 |

**Key Tables:** `ball_by_ball`, `matches`, `player`, `wicket_taken`, `extra_runs`, `player_match`, `season`, `venue`, `team`

---

## 🛠️ Tech Stack & Approach

```
MySQL (SQL Analysis)  →  CTEs  →  Window Functions  →  CASE WHEN  →  JOINs
```

**5 Custom KPIs Derived:**
- ⚡ Powerplay Run Rate
- 💀 Death Over Economy
- 🎯 Dot Ball Percentage
- 🏏 Boundary Percentage
- 📊 Composite Score (Avg × SR / 100)

---

## 📊 Key Analyses & Findings

### 🔥 Top Batsmen by Strike Rate (Min. 200 balls)

| # | Player | Strike Rate | Runs |
|---|--------|-------------|------|
| 1 | AB de Villiers | **163.74** | 1,955 |
| 2 | AD Russell | **163.16** | — |
| 3 | GJ Maxwell | **156.70** | — |
| 4 | KA Pollard | **142.86** | 1,320 |
| 5 | DA Warner | **141.02** | 2,348 |

> *AB de Villiers — highest volume AND highest aggression. Irreplaceable.*

---

### 📈 Most Consistent Batsmen (Min. 25 matches, Avg > 20)

| Player | Avg Runs | Matches | Total Runs |
|--------|----------|---------|------------|
| V Kohli | **39.87** | 62 | 2,472 |
| DA Warner | **38.49** | 61 | 2,348 |
| AB de Villiers | **34.53** | 57 | 1,968 |
| CH Gayle | **33.35** | 49 | 1,634 |
| AM Rahane | **32.40** | 57 | 1,847 |

---

### 🎳 Best Bowlers (Min. 10 matches)

| Player | Avg Wickets/Match | Total Wickets | Matches |
|--------|-------------------|---------------|---------|
| Imran Tahir | **2.21** | 31 | 14 |
| JD Unadkat | **2.09** | 23 | 11 |
| JJ Bumrah | **2.00** | 30 | 15 |
| UT Yadav | **2.00** | 56 | 28 |
| DJ Bravo | **1.93** | 81 ⬅ *highest total* | 42 |

---

### 🤝 Best All-Rounders (Above avg in both batting & bowling)

| Player | Avg Runs | Strike Rate | Avg Wickets |
|--------|----------|-------------|-------------|
| AD Russell | 22.91 | **163** | 1.84 |
| MP Stoinis | 29.20 | — | **2.25** |
| JP Faulkner | — | — | 1.91 |

> *22 players qualify as genuine all-rounders — all-rounders fill TWO roles per rupee at auction.*

---

### 🏟️ Venue Insights

| Venue | RCB Win % | Notes |
|-------|-----------|-------|
| M Chinnaswamy Stadium | **55.17%** | Strongest home ground |
| Wankhede Stadium | **25%** | Worst away ground |
| Rajiv Gandhi Uppal | **25%** | Avoid batting first |
| MA Chidambaram | **0%** | 0 wins in 2 matches |

**Toss Strategy:**
- Overall — fielding first wins **54.84%**
- At Chinnaswamy — fielding first wins **51.85%** vs **33.33%** batting first
- At Wankhede — **exception**: batting first wins **64.29%**

---

### 📉 Why Has RCB Never Won the IPL?

```
Season   Runs     Wickets   Win %
2013     ~2,460    78       56.25%
2014     1,992     —        35.71%   ← worst season
2015      —        —         —
2016     2,859    71        —        ← best batting ever, STILL lost the final

Batting peaked. Bowling collapsed.
SRH won 2016 with BOTH better runs AND wickets.
RCB always built a batting team. Never a championship team.
```

**Root cause: Bowling wickets declined every single season from 78 → 71 while batting improved.**

---

### 🏅 Man of the Match Leaders

| Player | MOTM Awards |
|--------|-------------|
| DA Warner | **11** |
| V Kohli | 9 |
| AB de Villiers | 9 |
| CH Gayle | 5 |

> *Dramatic drop after top 2 — RCB is dangerously over-reliant on Kohli and ABD.*

---

## 🏆 RCB Dream XI — 2017 Auction Strategy

| Order | Role | Player | Composite Score |
|-------|------|--------|-----------------|
| 1 | Opener | V Kohli | 54.09 |
| 2 | Opener | DA Warner | 54.25 |
| 3 | Middle Order | AB de Villiers | **56.72** |
| 4 | Middle Order | CH Gayle | — |
| 5 | All-rounder | AD Russell | 163 SR + 1.84 wkts |
| 6 | All-rounder | MP Stoinis | 29.2 avg + 2.25 wkts |
| 7 | Wicket-keeper | KD Karthik | 22.22 avg |
| 8 | Bowler | JJ Bumrah | 2.00 wkts/match |
| 9 | Bowler | SP Narine | 1.84 wkts + 6.24 econ |
| 10 | Bowler | Imran Tahir | 2.21 wkts/match |
| 11 | Bowler | UT Yadav | 2.00 wkts/match |

> 📐 *Composite Score = (Avg Runs × Strike Rate) / 100*

---

## 📁 Repository Structure

```
📦 RCB-IPL-Auction-Strategy-2017
 ┣ 📜 RCB_IPL_Completed_Script.sql     # All SQL queries (objective + subjective)
 ┣ 📄 RCB_IPL_Completed.docx           # Detailed analysis report with insights
 ┣ 📊 RCB_IPL_Completed.pptx           # Presentation deck
 ┗ 📖 README.md                        # You are here
```

---

## 🚀 How to Run

```sql
-- Step 1: Load the IPL database
SOURCE ipl_1.sql;
SOURCE ipl_2.sql;

-- Step 2: Select the database
USE ipl;

-- Step 3: Run the analysis script
SOURCE RCB_IPL_Completed_Script.sql;
```

**Requirements:** MySQL 8.0+

---

## 💡 Strategic Recommendations

1. 🔴 **Retain AB de Villiers** at any cost — only player with elite avg + elite strike rate combined
2. 🟡 **Target DA Warner** as Kohli's opening partner — both averaging 38+ across 60+ matches
3. 🎳 **Sign a quality wrist spinner** — high impact, low supply = better auction value
4. 🤝 **Prioritise all-rounders** — AD Russell & MP Stoinis fill two roles per rupee
5. 🏟️ **Venue-specific toss strategy** — field first at Chinnaswamy, bat first at Wankhede
6. ⚠️ **Avoid players above 32** — injury risk + premium auction price not justified by returns
7. 📊 **Use Composite Score model** — don't bid on hype, bid on (Avg × SR / 100)

---

## 👤 About the Author

**Shivam Gupta**
Data Analytics Program | Newton School | March 2026

[![GitHub](https://img.shields.io/badge/GitHub-Shivamgupta6388-181717?style=flat-square&logo=github)](https://github.com/Shivamgupta6388)

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=CC0000,FFD700&height=100&section=footer" width="100%"/>

*"The data doesn't lie — and RCB's data says bowling wins championships."*

⭐ **Star this repo if you found it useful!**

</div>
