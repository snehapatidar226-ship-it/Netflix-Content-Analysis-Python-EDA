# 🎬 Netflix Content Analysis — Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-4C8CBF)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Project Overview

This project performs an **Exploratory Data Analysis (EDA)** on Netflix's content library using the `netflix_titles_2021.csv` dataset. The goal is to uncover patterns in Netflix's content catalogue — including content type distribution, top contributing countries, yearly growth trends, ratings, and genre popularity.

This analysis demonstrates core data analytics skills: **data cleaning, transformation, univariate & bivariate analysis, and visualization**.

---

## 🎯 Objectives

- Understand the distribution of **Movies vs TV Shows** on Netflix
- Identify the **top countries** producing Netflix content
- Analyze **yearly content addition trends** over time
- Explore **content ratings** distribution
- Discover the **most popular genres/categories**
- Compare growth patterns of Movies vs TV Shows separately

---

## 📁 Project Structure

```
Netflix-EDA/
│
├── netflix_EDA.ipynb          # Main Jupyter Notebook with full analysis
├── netflix_titles_2021.csv    # Dataset (Netflix titles up to 2021)
└── README.md                  # Project documentation
```

---

## 📊 Dataset Information

| Field         | Details                                      |
|---------------|----------------------------------------------|
| **Source**    | Netflix Titles Dataset (2021)                |
| **File**      | `netflix_titles_2021.csv`                    |
| **Records**   | ~8,800 titles                                |
| **Columns**   | show_id, type, title, director, cast, country, date_added, release_year, rating, duration, listed_in, description |

---

## 🧹 Data Cleaning Steps

| Step | Action |
|------|--------|
| Missing Values | Dropped rows with null `date_added`; filled `director`, `cast`, `country` nulls with `'Unknown'` |
| Date Formatting | Stripped whitespace, parsed `date_added` to `datetime` using `"%B %d, %Y"` format |
| Feature Engineering | Extracted `year_added` from `date_added` for trend analysis |
| Data Copy | Worked on `df1 = df.copy()` to preserve original data |

---

## 📈 Analysis Performed

### 1. 🎥 Univariate Analysis
- **Movies vs TV Shows** — Count plot comparing content type distribution
- **Top 10 Countries** — Bar chart of countries contributing most content
- **Content Ratings** — Distribution of ratings (TV-MA, TV-14, R, PG-13, etc.)
- **Top 10 Genres** — Most frequently listed categories on Netflix

### 2. 📅 Bivariate Analysis
- **Yearly Content Addition Trend** — Line plot of total titles added per year
- **Movies Added Per Year** — Trend line for movie additions over time
- **TV Shows Added Per Year** — Trend line for TV show additions over time

---

## 🔍 Key Insights

- 📽️ **Movies dominate Netflix's catalogue** — significantly outnumber TV Shows
- 🇺🇸 **United States leads** content production, followed by India and the UK
- 📈 **Content additions grew rapidly from 2015–2019**, reflecting Netflix's global expansion phase
- 🔞 **TV-MA is the most common rating** — Netflix leans heavily toward mature content
- 🎭 **Dramas, Comedies, and Documentaries** are the top genres on the platform
- 📺 **TV Shows show steady growth** post-2016 as Netflix invested more in original series
- 📉 A slight dip in additions is visible post-2019, possibly due to COVID-19 production disruptions

---

## 🛠️ Technologies Used

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading, cleaning, transformation |
| `numpy` | Numerical operations |
| `matplotlib` | Base plotting and chart rendering |
| `seaborn` | Statistical visualizations (count plots) |
| `jupyter notebook` | Interactive development environment |

---

## ▶️ How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/snehapatidar226-shipit/Netflix-EDA.git
   cd Netflix-EDA
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```

3. **Launch Jupyter Notebook**
   ```bash
   jupyter notebook netflix_EDA.ipynb
   ```

4. **Update the dataset path** in Cell 2:
   ```python
   # Change this line to your local path or place CSV in the same folder
   df = pd.read_csv("netflix_titles_2021.csv")
   ```

---

## 📌 Sample Visualizations

> *(Add screenshots of your plots here after running the notebook)*

| Chart | Description |
|-------|-------------|
| `Movies vs TV Shows` | Count plot — content type distribution |
| `Top 10 Countries` | Bar chart — countries with most Netflix titles |
| `Yearly Trend` | Line plot — titles added per year (overall + split by type) |
| `Ratings Distribution` | Bar chart — content rating breakdown |

---

## 🚀 Future Scope

- [ ] Add NLP analysis on content descriptions
- [ ] Build a content recommendation system based on genres
- [ ] Analyze director/cast frequency and their content contribution
- [ ] Compare Netflix content strategy across different regions
- [ ] Interactive dashboard using Plotly or Power BI

---

## 👩‍💻 Author

**Sneha Patidar**  
📧 snehapatidar226@gmail.com  
🔗 [LinkedIn](https://linkedin.com/in/sneha-patidar-15bb73245)  
🐙 [GitHub](https://github.com/snehapatidar226-shipit)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

⭐ *If you found this project helpful, please give it a star!*
