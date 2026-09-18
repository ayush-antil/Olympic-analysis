# 120 Years of Olympic History: Trends Analysis

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1YrlnxsJ62Pgyt0AJmW1bIgrk3qpK3yA4)

## Project Overview

This project analyzes **271,116 athlete-event records** from the Olympic Games between **1896 and 2016**, covering both Summer and Winter Olympics.

The analysis explores long-term trends in Olympic participation, athlete demographics, countries, sports, events, and medal performance to understand how the Olympic Games have evolved over more than a century.

---

## Business Problem 

The objective of this project is to transform historical Olympic data into meaningful insights by identifying patterns in:

- Athlete participation
- Medal performance
- Country performance
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
- Which sports and events have the largest participation?
- How has female participation evolved over the years?
- What are the demographic characteristics of Olympic athletes?
- Which countries and sports have produced the most medal winners?
- How have Summer and Winter Olympics differed in participation and performance?
- Is there a relationship between athlete physical characteristics and medal success?

---

## Dataset

The project uses the `athlete_events.csv` dataset containing **271,116 athlete-event records** from Olympic Games held between **1896 and 2016**.

Each record contains information about:

- Athlete demographics
- Country and National Olympic Committee (NOC)
- Olympic Games and year
- Sport and event
- Medal results

---

## Analysis Performed

### Data Loading and Exploration

- Loaded the Olympic athlete-event dataset
- Examined dataset structure and dimensions
- Reviewed data types
- Analyzed missing values
- Identified meaningful and structural missing data

### Data Cleaning

- Handled missing medal values by treating them as no medal
- Examined missing values in athlete demographic variables
- Prepared the dataset for further analysis

### Feature Engineering

Created analytical features including:

- `Won_Medal`
- Age groups
- BMI
- Decade-based groupings
- Other analytical groupings using NumPy

### Medal Analysis

Analyzed:

- Overall medal win rate
- Medal win rate by gender
- Medal win rate by age group
- Gold, silver, and bronze medal distributions
- Top medal-winning athletes
- Country-level medal performance

### Participation Analysis

Analyzed:

- Olympic participation over time
- Male and female participation trends
- Summer versus Winter Olympic participation
- Sport and event participation

### Athlete Demographic Analysis

Analyzed:

- Athlete age
- Height
- Weight
- BMI
- Changes in physical profiles over time
- Relationship between physical characteristics and medal success

### Country and Sport Analysis

Analyzed:

- Country medal performance
- Sports with the highest medal counts
- Country performance across different Olympic seasons
- Historical participation patterns

---

## Key Findings

1. The overall medal win rate across recorded athlete-event participations was approximately **14.67%**.

2. Medal win rates differed slightly by gender, with female athletes showing a slightly higher observed rate than male athletes in this dataset.

3. Athletes in the **30–39 age group** had the highest observed medal win rate among the major age groups, while younger athletes had lower rates.

4. Physical characteristics alone do not strongly explain medal success, as overall BMI differences between medalists and non-medalists are relatively small.

5. Elite Olympic success can be highly concentrated among exceptional athletes, with **Michael Phelps** standing far above other athletes in total and gold-medal counts.

6. Rate-based metrics require sample-size awareness, particularly when analyzing historical sports or events with very few participants.

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

You can also open the notebook directly using the link below:

[Open Olympic Analysis in Google Colab](https://colab.research.google.com/drive/1YrlnxsJ62Pgyt0AJmW1bIgrk3qpK3yA4)

### How to Run

1. Open the notebook in Google Colab.
2. The required `athlete_events.csv` dataset is downloaded automatically during notebook execution.
3. Select **Runtime → Run all**.
4. Wait for all cells to finish executing.
5. Explore the analysis, visualizations, findings, and conclusions.

No manual dataset upload is required.

---

## Project Structure

- `README.md` — Project documentation
- `Olympic Analysis.ipynb` — Complete Olympic data analysis notebook

---

## Tools & Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Exploratory Data Analysis
- Feature Engineering
- Data Visualization
- Data Aggregation

---
