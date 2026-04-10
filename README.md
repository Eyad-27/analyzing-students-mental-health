# 🧠 Analyzing Students' Mental Health

![Mental Health Image](mentalhealth.jpg)

Does going to university in a different country affect your mental health? A Japanese international university surveyed its students in 2018 and published a study indicating that international students have a higher risk of mental health difficulties. 

This project uses **PostgreSQL** to explore the `students` data and determine if the length of stay is a contributing factor to mental health diagnostic scores.

---

## 📌 Guiding Questions
- How does the length of stay impact the average mental health scores of international students?
- Is there a visible trend in depression (PHQ-9), social connectedness (SCS), or acculturative stress (ASISS) based on time spent abroad?

---

## 📂 The Data

**`students.csv`** — contains survey results with the following features:

| Field Name     | Description                                      |
| -------------- | ------------------------------------------------ |
| `inter_dom`    | Types of students (international or domestic)    |
| `japanese_cate`| Japanese language proficiency                    |
| `english_cate` | English language proficiency                     |
| `academic`     | Current academic level (undergraduate or graduate)|
| `age`          | Current age of student                           |
| `stay`         | Current length of stay in years                  |
| `todep`        | Total score of depression (PHQ-9 test)           |
| `tosc`         | Total score of social connectedness (SCS test)   |
| `toas`         | Total score of acculturative stress (ASISS test) |

---

## 🛠️ Project Steps

### 1. Performing Calculations
- Counted the international students (`count_int`) and found summary statistics for each diagnostic test.
- Used `AVG()` to find the mean scores for the PHQ-9, SCS, and ASISS tests.
- Applied the `ROUND()` function to reduce the average scores to two decimal places.

### 2. Filter and Group the Data
- Applied a `WHERE` filter to focus exclusively on the **international** student group (`inter_dom = 'Inter'`).
- Grouped the data by the `stay` column to observe how scores change based on the length of residency.

### 3. Ordering Records
- Sorted the resulting table by the length of stay in **descending order** to compare long-term vs. short-term impacts.

---

## ✅ Key Deliverables
- A professional summary table with nine rows and five columns: `stay`, `count_int`, `average_phq`, `average_scs`, and `average_as`.
- Identification of whether longer stays correlate with higher or lower mental health risk.
- Optimized PostgreSQL queries with clear aliasing for easy data interpretation.

---

## 🧰 Skills Used
- SQL (PostgreSQL)
- Data Aggregation (`AVG`, `COUNT`)
- Data Filtering (`WHERE`)
- Data Formatting (`ROUND`, `ALIASING`)
- Data Sorting (`ORDER BY DESC`)
