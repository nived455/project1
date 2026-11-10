# Exploratory Data Analysis (EDA) on Titanic Dataset

**Internship:** InternCircle — Data Science & AI  
**Project:** 01 — Exploratory Data Analysis (EDA)  
**Author:** Nived Krishna B  

---

## 📌 Project Overview
This project performs an exploratory data analysis on the classic Titanic passenger dataset using Python and Pandas[cite: 1]. The primary goal is to inspect the data structure, clean missing values, handle categorical formats, and aggregate survival metrics to determine key demographic and socioeconomic survival factors[cite: 1, 2].

---

## 🎯 Guiding Questions
1. **Gender:** Did women survive at a significantly higher rate than men[cite: 1]?
2. **Class:** How strongly did passenger ticket class (`pclass`) correlate with survival[cite: 1]?
3. **Age:** Was age related to survival across different stages of life[cite: 1]?

---

## 🛠️ Data Cleaning & Preprocessing
* **Missing Value Imputation:**
  * `age`: Filled using the median age grouped by passenger class (`pclass`) and gender (`sex`) to account for socioeconomic age variations while avoiding outlier skew[cite: 2].
  * `embarked` / `embark_town`: Filled with the statistical mode (`S` / Southampton) as only two entries were missing[cite: 2].
  * `deck`: Dropped completely because over 77% (688 rows) of its records were missing[cite: 2].
* **Feature Engineering:**
  * Created an `age_band` feature using `pd.cut` with intervals `[0, 12, 18, 40, 60, 100]` corresponding to `Child`, `Teen`, `Adult`, `Middle-aged`, and `Senior`[cite: 2, 3].
* **Type Optimization:**
  * Converted categorical attributes (`sex`, `embarked`, `who`, `embark_town`, `alive`) into category data types[cite: 2].

---

## 📊 Key Findings & Written Summary
1. **Gender:** Female passengers survived at approximately **74%** (314 passengers) compared to about **19%** for male passengers (577 passengers)[cite: 2, 3].
2. **Ticket Class:** Higher socioeconomic class was strongly associated with survival: first-class passengers survived at **63%**, second-class at **47%**, and third-class at **24%**[cite: 3].
3. **Age Bands:** Children (0–12 years) had the highest survival rate across age groups at **58%**, adults (18–40 years) survived at **36%**, and seniors (60+ years) recorded the lowest survival rate at **23%**[cite: 3].

---

## 💻 Tech Stack
* **Language:** Python 3.13[cite: 1]
* **Libraries:** Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn, Jupyter[cite: 1]
* **Environment:** Visual Studio Code[cite: 1]

---

## 🚀 How to Run Locally
1. Clone the repository:
   ```bash
   git clone [https://github.com/nived455/project1.git](https://github.com/nived455/project1.git)
   cd project1
