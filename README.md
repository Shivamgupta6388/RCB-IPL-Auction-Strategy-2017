<div align="center">

<!-- Banner -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=CC0000,FFD700&height=200&section=header&text=RCB%20IPL%20Auction%20Strategy&fontSize=40&fontColor=fff&animation=fadeIn&fontAlignY=35&desc=Data-Driven%20Player%20Selection%20for%202017%20Mega%20Auction&descAlignY=55&descSize=16" width="100%"/>

# 🏏 IPL Data Analysis — Royal Challengers Bangalore
### Auction Strategy 2017 | SQL + Data Analytics Project

[![Author](https://img.shields.io/badge/Author-Shivam%20Gupta-CC0000...)](https://github.com/Shivamgupta6388)
[![Institute](https://img.shields.io/badge/Institute-Newton%20School-FFD700?style=for-the-badge)](https://newtonschool.co)
[![SQL](https://img.shields.io/badge/SQL-MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![Status](https://img.shields.io/badge/Status-Completed-00C853?style=for-the-badge)](/)

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

### 🔥 Top 3 Batsmen by Strike Rate (Min. 200 balls)

| # | Player | Strike Rate | Runs |
|---|--------|-------------|------|
| 1 | AB de Villiers | **163.74** | 1,955 |
| 2 | AD Russell | **163.16** | — |
| 3 | GJ Maxwell | **156.70** | — |

> *AB de Villiers — highest volume AND highest aggression. Irreplaceable.*

---

### 📈 Most Consistent Batsmen (Min. 25 matches, Avg > 20)

| Player | Avg Runs | Matches |
|--------|----------|---------|
| V Kohli | **39.87** | 62 |
| DA Warner | **38.49** | 61 |
| AB de Villiers | **34.53** | 57 |
| CH Gayle | **33.35** | 49 |

---

### 🎳 Best Bowlers (Min. 10 matches)

| Player | Avg Wickets/Match | Total Wickets |
|--------|-------------------|---------------|
| Imran Tahir | **2.21** | 31 |
| JJ Bumrah | **2.00** | 30 |
| UT Yadav | **2.00** | 56 |
| DJ Bravo | **1.93** | 81 ← *highest total* |

---

### 🏟️ Venue Insights

- **M Chinnaswamy Stadium** — RCB wins **55.17%** at home (strongest ground)
- **Wankhede Stadium** — Only **25%** win rate (worst away ground)
- **Toss Strategy** — Fielding first wins **54.84%** overall; at Chinnaswamy, fielding first wins **51.85%** vs only **33.33%** batting first

---

### 📉 Why Has RCB Never Won the IPL?

```
Batting peaked in 2016 → 2,859 runs (best ever season)
BUT... Wickets declined every year → 78 (2013) → 71 (2016)

SRH won 2016 with BOTH better runs AND wickets.
RCB's bowling gets weaker as their batting improves.
```

**The core problem: Batting-heavy squad with no bowling depth.**

---

## 🏆 RCB Dream XI — 2017 Auction Strategy

| Order | Role | Player | Composite Score |
|-------|------|--------|-----------------|
| 1 | Opener | V Kohli | 54.09 |
| 2 | Opener | DA Warner | 54.25 |
| 3 | Middle Order | AB de Villiers | **56.72** |
| 4 | Middle Order | CH Gayle | — |
| — | All-rounder | AD Russell | (163 SR + 1.84 wkts) |
| — | All-rounder | MP Stoinis | (29.2 avg + 2.25 wkts) |
| — | Bowler | JJ Bumrah | 2.00 wkts/match |
| — | Bowler | SP Narine | 1.84 wkts + 6.24 econ |

> *Composite Score = (Avg Runs × Strike Rate) / 100*

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

## 💡 Strategic Recommendations Summary

1. **Retain AB de Villiers** at any cost — only player combining elite average + elite strike rate
2. **Target DA Warner** as opening partner for Kohli — both averaging 38+ across 60+ matches
3. **Sign a quality wrist spinner** — high impact, low supply = better auction price
4. **Prioritise all-rounders** — AD Russell and MP Stoinis fill two roles per rupee
5. **Venue-specific toss strategy** — field first at Chinnaswamy, bat first at Wankhede
6. **Avoid over-25 players above 32** — injury risk + premium auction price not justified

---

## 👤 About

**Shivam Gupta** | Data Analytics Program, Newton School | March 2026

---

<div align="center">
<img src="https://capsule-render.vercel.app/api?type=waving&color=CC0000,FFD700&height=100&section=footer" width="100%"/>

*"The data doesn't lie — and RCB's data says bowling wins championships."*

⭐ **Star this repo if you found it useful!**

</div>
