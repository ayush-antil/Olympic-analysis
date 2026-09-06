# 120 Years of Olympic History: Trends Analysis

## Overview
Analysis of 271,116 Olympic athlete records spanning 1896–2016, covering medal success by demographic, 
country performance across Summer vs. Winter Games, and historical trends in athlete physical profiles.

## What I Did
- Handled "meaningful missingness" correctly — distinguished between genuine missing data (Age/Height/Weight) 
  and structurally meaningful nulls (Medal, where missing means "did not medal," not "data quality issue")
- Engineered features using NumPy (`np.where`, `np.select`): binary medal flag, age brackets, decade 
  groupings, BMI
- Caught and corrected a small-sample distortion in raw per-age win rates (e.g., a misleading 100% win rate 
  from a single athlete) by bucketing into age groups instead
- Investigated a real data-quality issue: found that using `Team` instead of `NOC` for country rankings 
  produces genuinely different, incorrect results — including flipping which country actually leads Winter 
  Olympics medals
- Analyzed Summer vs. Winter performance separately, rather than combining fundamentally different competitions

## Key Results
- Overall medal win rate: **14.67%**, with women winning at a slightly higher rate (15.1%) than men (14.5%)
- The **30-39 age bracket** has the highest win rate (16.1%) — challenging the assumption that athletes peak 
  in their early-to-mid 20s
- **USA leads medal counts in both Summer and Winter Olympics** — the only country to top both seasons
- Using `Team` (1,184 unique values) instead of `NOC` (230 unique values) for country rankings incorrectly 
  showed Canada leading Winter Olympics — the correct `NOC`-based ranking shows USA actually leads
- **Michael Phelps holds the most total medals (28)**, overwhelmingly gold-heavy (23 gold), unlike other top 
  medalists whose totals are more evenly split across Gold/Silver/Bronze
- Age, Height, and Weight all follow a **U-shaped trend** across 12 decades, tied to the Olympics' own 
  historical expansion

## Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn
