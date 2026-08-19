# ⚽ FIFA World Cup - Exploratory Data Analysis (EDA)

A comprehensive data analysis project examining historical FIFA World Cup tournament matches, team distributions, and performance trends using Python and Pandas.

## 📊 Project Objectives
* Extract and structure historical tournament match results into descriptive formats.
* Analyze victory statistics across distinct knockout stages (Quarter-finals, Semi-finals, Finals).
* Calculate historical win probabilities for major national teams.
* Design meaningful data visualizations to expose tournament patterns over time.

## ⚙️ Core Implementation Details
The project utilizes an elegant, modular workflow:
* **Dynamic Data Filtering:** Filters data row-by-row matching a target country across both home and away game scenarios.
* **Knockout Stage Isolation:** Extracts records matching standard knockout rounds using custom vector filtering techniques.
* **Custom Win Metrics Extraction:** Features a built-in automated match assessment function:
  ```python
  def get_winner(row):
      if row['h_total'] > row['a_total']:
          return row['home_team']
      else:
          return row['away_team']
  ```
* **Performance Metric Merges:** Aggregates and converts frequency indexes to evaluate dynamic aggregate metrics.

## 🎯 Analytical Insights & Conclusions
Based on the programmatic evaluation of historical tournament phases, key patterns include:

* **🇮🇹 Italy:** Teams facing Italy in knockout rounds encounter defensive resilience. Italy exhibits a **75% probability** of winning in the quarter-finals, an **86% probability** of advancing from the semi-finals, and a **67% probability** of securing a victory in the finals.
* **🇪🇸 Spain:** Historically, if Spain successfully clears the Quarter-final stage, they carry an exceptionally high statistical probability of securing the championship title.
* **🇫🇷 France:** Display an excellent, dominant record during the Quarter-finals phase, though historical conversion rates drop slightly during subsequent Semi-final and Final matches.
* **🇸🇪 Sweden:** While achieving competitive consistency in earlier phases, historically encounters a bottleneck before reaching final matches.

## 🛠️ Tech Stack & Libraries
* **Language:** Python
* **Environment:** Jupyter Notebook (`.ipynb`)
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:**
  * 📈 **Matplotlib:** Used for establishing core chart structures, figures, and plots.
  * 🎨 **Seaborn:** Used for generating clean statistical plots, distributions, and heatmaps.
  * 🚀 **Plotly:** Used for building fully interactive, zoomable, and dynamic charts for deeper data exploration.
