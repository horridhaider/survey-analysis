<div align="center">

# 💼 Ask A Manager — Salary Survey Analysis

### *Uncovering the truth behind 28,000+ real-world salaries*

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-22C55E?style=for-the-badge)](LICENSE)

---

> *What does a Software Engineer in Australia really earn compared to one in Canada?  
> Does a PhD actually pay off? Does the gender pay gap widen after 3 years?  
> This project answers all that — and more — with data.*

---

</div>

## 📖 The Story Behind This Project

Every year, thousands of professionals anonymously share their salaries on *Ask A Manager* — one of the most trusted workplace advice platforms on the internet. The **2021 edition** collected over **28,000 responses** spanning dozens of countries, industries, genders, and education levels.

This project takes that raw, messy, human-reported data and transforms it into **clear, visual answers** to the questions professionals actually ask:

- *Am I being underpaid for my experience?*
- *Which field should I move into for better pay?*
- *Does where I live really matter that much?*

No fluff. No guesswork. Just honest analysis backed by real numbers.

---

## ✨ What This Analysis Covers

| # | Question Explored | What You'll Discover |
|---|---|---|
| 🏭 | **Which industry pays the most?** | Top 20 highest-paying fields, ranked by average USD salary |
| 📈 | **Does experience always mean more money?** | How salaries climb — or plateau — across career stages |
| 🌍 | **Same job, different country — how big is the gap?** | Side-by-side salary comparison for the same roles across 10 countries |
| ⚧ | **Is the gender pay gap real, and when does it kick in?** | How the gap between Male, Female, and Non-binary salaries evolves with experience |
| 🎓 | **Does education + race play a role in earnings?** | A heatmap breakdown of average salaries by race and education level |

---

## 🗂️ Project Structure

```
survey-analysis/
│
├── 📓 survey-analysis.ipynb     ← Main notebook: cleaning, EDA, and all 5 analyses
│
├── 📁 data/
│   └── salary_survey.xlsx       ← Raw survey data (28,000+ rows, as downloaded)
│
├── 📁 output/                   ← Auto-generated after running the notebook
│   └── clean_survey.xlsx        ← Cleaned dataset (two sheets: Clean + Dirty)
│
├── 📁 plots/                    ← Auto-generated visualizations (PNG, 300 DPI)
│   ├── salary_distribution_in_industries.png
│   ├── top_dept_avg_salary_barh.png
│   ├── salary_experience_plot.png
│   ├── avg_salary_dept_country.png
│   ├── salary_gender_experience_plot.png
│   ├── avg_salary_race_education.png
│   └── salary_race_education_heatmap.png
│
├── 📁 report/                   ← Summary report and findings
├── 📄 requirements.txt          ← Python dependencies
├── 📄 .gitignore
└── 📄 LICENSE
```

> **Note:** The `output/` and `plots/` folders are created automatically when you run the notebook — no manual setup needed.

---

## 🔬 How the Data Was Cleaned

Raw survey data is notoriously messy — especially when 28,000 people are typing their own answers. Here's what was tackled before a single chart was drawn:

- **🗑️ Dropped irrelevant columns** — Removed `job_context`, `other_currency`, `income_context`, and `overall_experience` to keep the dataset lean and focused.
- **🌐 Standardised country names** — `"u.s.a"`, `"Unites States"`, `"🇺🇸"`, and 25+ other variations were all mapped back to `"United States"`.
- **🏭 Simplified industry & department labels** — Long, inconsistent entries were trimmed to their first three meaningful words and title-cased.
- **⚧ Cleaned gender categories** — `"Man"` → `"Male"`, `"Woman"` → `"Female"`, ambiguous responses → `"Other"`.
- **🎭 Fixed race entries** — Extracted the primary racial identity from mixed/lengthy responses.
- **📅 Converted experience brackets to numbers** — `"5 - 7 years"` became `6.0` (the average), enabling proper numerical analysis.
- **💰 Currency normalisation** — All 11 currencies (GBP, EUR, CAD, AUD, CHF, ZAR, SEK, HKD, JPY, AUD/NZD) converted to USD using 2021 exchange rates.
- **📊 Outlier removal** — Extreme values filtered using the IQR method to prevent skewed visuals.
- **🧹 Missing values handled** — Rows with critical nulls dropped; less critical fields filled with sensible defaults (`"No Bonus"`, `"N/A"`).

---

## 📊 Key Findings at a Glance

<table>
<tr>
<td width="50%">

### 🏆 Top-Paying Industries
Compensation & Benefits, Technology, and Law consistently rank at the top. Respondents in these sectors average **$30–50K more per year** than those in Education or Non-profit.

</td>
<td width="50%">

### 📈 Experience vs. Salary
Salaries grow steadily through mid-career, with the steepest jump occurring between **3–15 years** of experience. Beyond 22 years, growth levels off for most groups.

</td>
</tr>
<tr>
<td width="50%">

### 🌍 Location Premium is Real
The United States consistently tops country-level pay rankings across most departments. However, **Switzerland and the UK** compete closely in Finance and Law roles.

</td>
<td width="50%">

### ⚧ The Gender Pay Gap Widens Over Time
At entry level, salary differences between Male and Female respondents are modest. By **15+ years of experience**, the gap becomes substantial — Male salaries nearly double, while Female growth is more gradual.

</td>
</tr>
</table>

---

## 🚀 Getting Started

### Prerequisites

Make sure you have **Python 3.8+** installed. Then clone this repo and install the required packages:

```bash
# 1. Clone the repository
git clone https://github.com/horridhaider/survey-analysis.git
cd survey-analysis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch Jupyter
jupyter notebook survey-analysis.ipynb
```

That's it. Run all cells from top to bottom — the `output/` and `plots/` directories will be created automatically.

---

## 🛠️ Built With

| Tool | Purpose |
|---|---|
| **Python 3.8+** | Core programming language |
| **Pandas** | Data loading, cleaning, and transformation |
| **NumPy** | Numerical operations and outlier calculations |
| **Matplotlib** | All chart generation and figure styling |
| **Seaborn** | Heatmap visualisation (race × education) |
| **OpenPyXL** | Reading and writing `.xlsx` Excel files |

---

## 📂 Data Source

The raw dataset is sourced from the **Ask A Manager 2021 Salary Survey**:

> 📎 [Ask A Manager Salary Survey 2021 (Google Sheets)](https://docs.google.com/spreadsheets/d/1IPS5dBSGtwYVbjsfbaMCYIWnOuRmJcbequohNxCyGVw/edit?resourcekey=&gid=1625408792#gid=1625408792)

The survey is self-reported, voluntary, and anonymous. Results reflect the experiences of respondents — primarily English-speaking professionals — and may not represent global averages.

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

You're free to use, adapt, and build upon this work for personal or commercial purposes, with attribution.

---

<div align="center">

Made with 🐍 Python · 📊 Data · ☕ Coffee

**[⭐ Star this repo](https://github.com/horridhaider/survey-analysis)** if you found it useful!

</div>
