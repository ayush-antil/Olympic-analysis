# 120 Years of Olympic History: Trends Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1YrlnxsJ62Pgyt0AJmW1bIgrk3qpK3yA4)

## Project Overview

This project analyzes **271,116 athlete-event records** from the Olympic Games between **1896 and 2016**, covering both Summer and Winter Olympics.

The analysis explores long-term trends in Olympic participation, athlete demographics, country performance, sports, events, and medal success to understand how the Olympic Games have evolved over more than a century.

---

## Business Problem

The objective of this project is to transform historical Olympic data into meaningful insights by identifying patterns in:

- Athlete participation
- Medal performance
- Country-level performance
- Gender participation
- Athlete demographics
- Sports and events
- Historical changes over time

The analysis focuses on using data exploration, feature engineering, aggregation, and visualization to understand Olympic participation and performance patterns.

---

## Key Questions

This analysis focuses on questions such as:

- How has Olympic participation changed over time?
- Which countries have achieved the highest medal success?
- How does medal win rate vary by gender and age group?
- How has female participation evolved over the history of the Games?
- Which countries perform best in Summer versus Winter Olympics?
- What relationship exists between athlete physical characteristics and medal success?
- Which athletes have won the most Olympic medals?
- Which sports have the highest medal win rates, and how should small sample sizes be considered?

---

## Dataset

The project uses the `athlete_events.csv` dataset containing **271,116 athlete-event records** from Olympic Games held between **1896 and 2016**.

Each record contains information about:

- Athlete demographics
- Sex
- Age
- Height
- Weight
- Team
- National Olympic Committee (NOC)
- Olympic Games
- Year
- Season
- City
- Sport
- Event
- Medal result

---

## Data Quality & Preprocessing

The dataset contains missing values in several demographic fields:

- `Age`: 9,474 missing values
- `Height`: 60,171 missing values
- `Weight`: 62,875 missing values
- `Medal`: 231,333 missing values

The project distinguishes between genuine missing data and **meaningful missingness**.

Missing `Medal` values represent athletes who did not receive a medal rather than a data-quality problem. These values were therefore converted to `No Medal` instead of removing the records.

The analysis also creates a binary `Won_Medal` feature to simplify medal-success calculations.

---

## Analysis Performed

### Data Loading & Exploration

- Loaded the complete Olympic athlete dataset
- Examined dataset structure and dimensions
- Inspected data types
- Analyzed missing values
- Reviewed descriptive statistics

### Feature Engineering

Created analytical features including:

- `Won_Medal` — binary indicator of whether an athlete won a medal
- `Age_Group` — grouped athletes into meaningful age brackets
- `Decade` — used for long-term historical comparisons
- `BMI` — calculated from athlete height and weight

### Medal Success Analysis

Analyzed medal win rates across:

- Overall participation
- Gender
- Age groups
- Sports
- Countries
- Olympic seasons

### Country Performance

Identified the countries with the highest total medal counts and compared country performance between:

- Summer Olympics
- Winter Olympics

### Participation Trends

Analyzed how Olympic participation changed over time, including:

- Overall participation growth
- Female participation
- Male participation
- Historical changes across Olympic Games

### Athlete Demographics

Examined long-term changes in:

- Average athlete age
- Average height
- Average weight
- BMI

These characteristics were compared across Olympic decades.

### Athlete-Level Analysis

Identified the most decorated Olympic athletes by:

- Total medals
- Gold medals
- Silver medals
- Bronze medals

Medal composition was also analyzed to distinguish overall podium consistency from gold-medal dominance.

---

## Key Findings

### Overall Medal Win Rate

The overall medal win rate across the **271,116 athlete-event records** is **14.67%**, meaning approximately 1 in 7 recorded participations resulted in a medal.

### Medal Win Rate by Gender

Medal win rates were:

| Gender | Medal Win Rate |
|---|---:|
| Women | 15.1% |
| Men | 14.5% |

The difference is small but remains visible when Summer and Winter Olympics are analyzed separately.

### Medal Win Rate by Age

The **30–39 age group** recorded the highest medal win rate at **16.1%**, followed by the **20–29 group at 15.5%**.

The Under 20 group recorded a lower win rate of **10.6%**, while the 40+ group recorded **13.8%**.

This suggests that Olympic medal success is not necessarily concentrated in the youngest athlete groups and that experience may play an important role in many sports.

### Country Performance

The **USA leads total historical medals with 5,637**, followed by:

1. USA — 5,637
2. URS — 2,503
3. GER — 2,165
4. GBR — 2,068
5. FRA — 1,777

Historical NOC codes such as `URS` represent countries or political entities that no longer exist in their original form, so historical rankings require appropriate context.

### Summer vs. Winter Olympics

The USA ranks first in both Summer and Winter Olympic medal totals.

**Summer Olympics — Top 5:**

1. USA — 5,002 medals
2. URS — 2,063 medals
3. GBR — 1,985 medals
4. GER — 1,779 medals
5. FRA — 1,627 medals

**Winter Olympics — Top 5:**

1. USA — 635 medals
2. CAN — 611 medals
3. NOR — 443 medals
4. URS — 440 medals
5. SWE — 428 medals

The different country rankings demonstrate the distinct competitive profiles of Summer and Winter Olympic sports.

### Women's Participation

Women's participation increased dramatically throughout Olympic history.

The dataset records **no female participation in 1896** and only **23 female athletes in 1900**, while participation grew to thousands of female athletes in recent Games.

This is one of the most significant long-term trends identified in the analysis.

### Athlete Physical Profile

Average athlete age, height, and weight show a broadly **U-shaped pattern across the analyzed decades**.

Average age increased from approximately **23.6 in the 1890s** to around **29.0 in the 1930s**, declined through the middle of the century, and increased again to approximately **26.1 in the 2010s**.

Height and weight show similar long-term changes, with modern athletes showing a modest increase compared with the mid-century period.

### BMI and Medal Success

Average BMI was:

| Group | Average BMI |
|---|---:|
| Medalists | 23.16 |
| Non-medalists | 22.72 |

The small difference suggests that BMI alone is not a strong predictor of Olympic medal success because athlete physiques vary substantially across different sports.

### Most Decorated Athlete

**Michael Phelps** leads the overall medal rankings with **28 Olympic medals**, including:

- 23 Gold
- 3 Silver
- 2 Bronze

The next athlete in the overall ranking has 18 medals.

Phelps' medal total is particularly notable because the majority of his medals are gold, demonstrating not only repeated podium finishes but exceptional first-place performance.

### Sport-Level Win Rates

Some sports show extremely high or even **100% medal win rates**.

However, these results can be misleading when the sport has only a very small number of historical participants or was held only once.

Therefore, sport-level win rates should always be interpreted alongside participant counts and historical context.

---

## Business & Analytical Insights

1. **Olympic participation expanded dramatically over time**, particularly female participation, reflecting the increasing scale and inclusiveness of the Games.

2. **Medal success varies across demographic groups**, with the 30–39 age group showing the highest observed medal win rate in this dataset.

3. **Country performance differs substantially between Summer and Winter Olympics**, highlighting the importance of analyzing competitions separately rather than relying only on combined rankings.

4. **Physical characteristics alone do not strongly explain medal success**, as overall BMI differences between medalists and non-medalists are relatively small.

5. **Elite Olympic success can be highly concentrated among exceptional athletes**, with Michael Phelps standing far above other athletes in total and gold-medal counts.

6. **Rate-based metrics require sample-size awareness**, particularly when analyzing historical sports or events with very few participants.

---


```markdown
---

## Project Workflow

**Data Loading**  
↓  
**Data Inspection**  
↓  
**Missing-Value Analysis**  
↓  
**Data Cleaning**  
↓  
**Feature Engineering**  
↓  
**Medal Win Rate Analysis**  
↓  
**Gender & Age Analysis**  
↓  
**Country Performance Analysis**  
↓  
**Participation Trends**  
↓  
**Athlete Physical Profile Analysis**  
↓  
**BMI vs. Medal Success**  
↓  
**Summer vs. Winter Analysis**  
↓  
**Athlete-Level Medal Analysis**  
↓  
**Insights & Conclusions**

---

## Run the Project

The complete analysis is available as a Google Colab notebook.

### Open in Google Colab

Click the **Open in Colab** button at the top of this README to open the notebook.

Alternatively, use the link below:

**[Open Olympic Analysis in Google Colab](https://colab.research.google.com/drive/1YrlnxsJ62Pgyt0AJmW1bIgrk3qpK3yA4)**

### How to Run

1. Open the notebook in Google Colab.
2. The required `athlete_events.csv` dataset is downloaded automatically during notebook execution.
3. Select **Runtime → Run all**.
4. Wait for all cells to finish executing.
5. Explore the visualizations, analysis, findings, and conclusions.

No manual dataset upload is required.

---

## Project Structure

```text
├── README.md
└── Olympic Analysis.ipynb
