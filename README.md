# ICC_t20_WC_24
Developed a data pipeline that scrapes Cricket World Cup data from the ICC website, processes it, and visualizes performance metrics of teams and players in Power BI

---

## 📌 Project Overview

This project is divided into two main phases:

1. **Part 1 – Data Fetching & Cleaning (Jupyter Notebooks)**
2. **Part 2 – Power BI Dashboard Development**

---

## 🏏 Part 1: Data Fetching & Cleaning (Jupyter Notebooks)

It focuses on **automated data collection and cleaning** using Python to prepare match, batting, and bowling datasets for further analysis and visualization.

---

### 📌 Goals

- Programmatically fetch T20 World Cup 2024 match data
- Use Selenium to scrape detailed stats from match webpages
- Handle edge cases (e.g., rain-affected, tied/super over matches)
- Export clean and structured datasets for analysis and dashboarding

---

### 🛠️ Tools & Libraries Used

- `requests` – to retrieve base match data
- `selenium` – for automated web scraping from stats pages
- `pandas` – for data manipulation and cleaning
- `csv` – for exporting results

---
### 🧼 Data Cleaning Highlights

- Filtered out **rain-affected** and **no-result** matches
- Identified and tagged **super over** matches separately
- Standardized missing/erroneous values in batting and bowling data

---

### 📂 Output Files

- **`Matches.csv`** – Match metadata (date, venue, teams, result)
- **`BattingSummary.csv`** – Player-level batting stats
- **`BowlingSummary.csv`** – Player-level bowling stats
- **`TeamList.csv`** – Team list metadata(players, flag, player image, stats)

These files are used as input for the Power BI dashboard in the next phase.

---

## 📊 Part 2 – Power BI Dashboard Development

### 📆 Objective

To develop a dynamic and interactive **Power BI dashboard** using cleaned datasets to analyze team and player performance throughout the T20 World Cup 2024.

### 🔧 Technical Implementation

- **Data Import & Modeling**
  - Imported `.csv` files into Power BI Desktop
  - Created relationships between match, player, and team datasets

- **DAX Measures & KPIs**
  - Calculated total runs, wickets, centuries, and filtered rankings
  - Defined reusable DAX measures for cross-report consistency

- **Power Query**
  - Applied additional filtering and data transformations inside Power BI

### 📝 Report Pages

#### 1. **Top Performers**

- Visuals:
  - Top 3 Run Scorers
  - Top 3 Wicket Takers
  - Tournament-wide metrics: Total Runs, Total Centuries

#### 2. **Team Sheet**

- Team-wise performance tables:
  - Player list with total runs/wickets
  - Used **column charts** to visualize top players with highest **sixes** and **wickets**
  - Removed player images and team flags for a cleaner tabular experience

#### 3. **Player Sheet**

- Individual player performance:
  - Stats against each opponent
  - Fetched **player images** and **team flags** for identity reference
  - Used multiple visuals including **column charts**, **gauge charts**, and more for various KPIs

#### 4. **Compare Sheet**

- Head-to-head comparison of two selected players:
  - Performance breakdown per opponent
  - Useful for analytical comparison and decision support

### 🏋️ Output Highlights

- Fully interactive dashboard with slicers, drill-throughs, and responsive visuals
- Supports both **high-level summaries** and **granular breakdowns**
- Easily extensible for future match data or real-time updates

---

### 🛠️ Tools & Technologies

| Tool        | Purpose                                |
| ----------- | -------------------------------------- |
| Power BI    | Data modeling and dashboard creation   |
| DAX         | Metrics and custom calculations        |
| Power Query | In-app data shaping and transformation |
| CSV Files   | Input from Python-based ETL pipeline   |

---

## Result Dashboard

![Dashboard](/Result%20Images/Dashboard.JPG)

![Plyaer Stats](/Result%20Images/Player%20Stats.JPG)

![Team Comparison](/Result%20Images/Team%20comparison.JPG)

![Team Stats](/Result%20Images/Teams%20Stats.JPG)

## 👥 Contributors

- [Joel Stanly](https://github.com/JoelStanly)
- [Prasanth E](https://github.com/Prasanth121)

---

## 🚀 Usage

1. Clone the repository:
```https://github.com/JoelStanly/ICC_t20_WC_24.git```

2. Install the required Python packages:
``` pip install -r requirements.txt ```

3. Ensure Selenium WebDriver is installed

3. Run the Jupyter notebook 02_Data_Cleaning.ipynb

4. Output CSV files will be saved
    - matches.csv
    - batting_summary.csv
    - bowling_summary.csv
    - team_list.csv

These files can then be used directly in Power BI for further analysis.

---
Let me know if you're using Jupyter Lab or VS Code and want to customize the steps accordingly.

## 📜 License
This project is licensed under the MIT License.