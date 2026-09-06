# 🇮🇳 Indian Startups Funding Analysis

## 📌 Project Overview

This project analyzes **Indian startup funding data** to understand funding patterns, investment trends, popular sectors, investor behavior, investment types, funding distribution, and startup growth trajectories.

The analysis is performed using **Python, Pandas, NumPy, Matplotlib, and Seaborn**. The project follows a step-by-step data analytics workflow, starting from data inspection and preprocessing and progressing to exploratory and advanced analysis.

---

## 🎯 Objectives

The main objectives of this project are:

* Analyze startup funding trends over time.
* Identify the most funded startup sectors.
* Identify cities receiving significant startup funding.
* Find the most active investors.
* Analyze different investment types.
* Understand the relationship between sectors and investment types.
* Analyze the distribution of funding amounts and detect outliers.
* Identify sectors showing higher annual funding growth.
* Classify investors into different investor types.
* Track funding trajectories of highly funded startups.

---

## 📊 Dataset

The analysis uses an Indian startup funding dataset containing **2,372 records and 10 original columns**.

### Original Columns

| Column              | Description                    |
| ------------------- | ------------------------------ |
| `SNo`               | Serial number                  |
| `Date`              | Date of funding                |
| `StartupName`       | Name of the startup            |
| `Industry_Vertical` | Industry/sector of the startup |
| `SubVertical`       | Startup's specific sub-sector  |
| `City_Location`     | Location of the startup        |
| `Investors_Name`    | Names of investors             |
| `InvestmentType`    | Type/stage of investment       |
| `Amount_In_INR`     | Funding amount in INR          |
| `Remarks`           | Additional information         |

The notebook identifies missing values in several columns, particularly `SubVertical`, `Amount_In_INR`, and `Remarks`.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Google Colab** – Development environment
* **Excel** – Source dataset

---

## 🔄 Project Workflow

The notebook follows this analysis workflow:

### 1. Data Loading & Inspection

The startup funding Excel dataset is loaded into a Pandas DataFrame.

Initial inspection includes:

* Viewing the first records.
* Checking dataset structure.
* Checking column data types.
* Identifying missing values.
* Understanding the overall data quality.

---

### 2. Data Cleaning & Preprocessing

The dataset is prepared for analysis by:

* Handling missing industry values.
* Handling missing sub-vertical information.
* Handling missing city information.
* Handling missing investor information.
* Converting the `Date` column into datetime format.
* Extracting `Year` and `Month` from the date.
* Filling missing funding amounts using the median funding value.
* Standardizing selected sector names.

A cleaned dataset is also exported as:

```text
cleaned_startup_funding.csv
```

---

### 3. Funding Trends Over Time

The project analyzes how startup funding activity changes over time.

Visualizations include:

* Number of funding deals by year.
* Total funding amount by year.

These visualizations help understand changes in startup investment activity across different years.

---

### 4. Sector Analysis

The project identifies sectors with the highest startup funding activity.

Two major analyses are performed:

* Top sectors by **number of funding deals**.
* Top sectors by **total funding amount**.

This helps identify industries that attract both frequent investment and large amounts of capital.

---

### 5. Investor Analysis

Investor names are split when multiple investors are listed in a single record.

The analysis then identifies:

* Most active investors.
* Investors participating in the highest number of funding deals.

This provides insight into the investor landscape within the dataset.

---

### 6. Investment Type Analysis

The project analyzes different investment types used in startup funding.

A bar chart is created to visualize the frequency of investment types and understand which funding categories appear most frequently in the dataset.

---

### 7. Sector vs Investment Type Analysis

A cross-tabulation and heatmap are used to study the relationship between:

**Industry Sector × Investment Type**

The analysis focuses on the top sectors by activity and shows how different investment types are distributed across those sectors.

---

### 8. Funding Distribution & Outlier Analysis

The project examines the distribution of startup funding amounts using:

* Histogram
* Kernel Density Estimate (KDE)
* Boxplot

The boxplot is particularly useful for identifying unusually large funding amounts and potential outliers.

---

### 9. Sector Growth Analysis

The project calculates year-over-year changes in funding across sectors.

This analysis attempts to identify sectors with higher average annual funding growth and provides an indication of sectors that may have experienced strong changes in investment activity.

---

### 10. Advanced Investor Analysis

Investors are classified into broad categories using name-based rules:

* **VC**
* **Angel**
* **Corporate**
* **Other**

The distribution of these investor categories is visualized to understand the different types of investors participating in startup funding.

> Note: Investor classification is rule-based and depends on keywords contained in investor names.

---

### 11. Startup Funding Trajectory

The project tracks funding for startups over different years.

The analysis:

1. Groups funding by startup and year.
2. Calculates yearly funding totals.
3. Identifies the top 5 startups based on total funding.
4. Plots their funding trends over time.

This helps visualize how funding for highly funded startups changed across the available years.

---

## 📈 Visualizations

The notebook generates several visualizations, including:

* 📊 Funding Deals by Year
* 📈 Total Funding by Year
* 📊 Top Sectors by Number of Deals
* 💰 Top Sectors by Total Funding
* 👥 Top Investors by Number of Deals
* 💼 Investment Type Distribution
* 🔥 Sector vs Investment Type Heatmap
* 📉 Funding Amount Distribution
* 📦 Funding Amount Outlier Boxplot
* 📈 Sector Funding Growth
* 👤 Investor Type Distribution
* 🚀 Startup Funding Growth Over Time

---

## 📁 Project Structure

```text
Indian-Startups-Analysis/
│
├── Indian_Startups_Analysis.ipynb
├── startup_funding138.xlsx
├── cleaned_startup_funding.csv
└── README.md
```

> The exact source Excel filename used in the notebook is `startup_funding138 (1).xlsx`.

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Install the required libraries

```bash
pip install pandas numpy matplotlib seaborn openpyxl
```

### 3. Open the notebook

Open:

```text
Indian_Startups_Analysis.ipynb
```

using:

* Google Colab
* Jupyter Notebook
* JupyterLab
* VS Code

### 4. Add the dataset

Place the startup funding Excel file in the expected location or update the dataset path in the notebook.

The notebook currently loads the Excel file using Pandas.

### 5. Run all cells

Execute the notebook cells sequentially to reproduce the analysis and visualizations.

---

## 🔍 Key Analytical Areas

| Area                  | Analysis                                 |
| --------------------- | ---------------------------------------- |
| Dataset               | Structure & missing values               |
| Preprocessing         | Missing-value handling & date conversion |
| Time Analysis         | Yearly funding & deal counts             |
| Sector Analysis       | Top sectors                              |
| Investor Analysis     | Most active investors                    |
| Investment Analysis   | Investment types                         |
| Relationship Analysis | Sector vs investment type                |
| Statistical Analysis  | Distribution & outliers                  |
| Growth Analysis       | Sector funding growth                    |
| Advanced Analysis     | Investor classification                  |
| Startup Analysis      | Funding trajectories                     |

---

## ⚠️ Data Processing Notes

The notebook uses median imputation for missing values in `Amount_In_INR`.

Missing categorical values are replaced with labels such as:

```text
Others
Not Specified
Undisclosed
```

The notebook also creates a new `Sub_Vertical` column from the existing `SubVertical` column. When reproducing or improving the project, this naming inconsistency should be cleaned up so that only one sub-vertical column is maintained.

Investor classification is based on keywords such as `capital`, `ventures`, `partners`, `fund`, `angel`, `network`, `ltd`, and similar terms. Therefore, the classification should be considered an analytical approximation rather than a verified investor-type database.

---

## 💡 Possible Future Improvements

The project can be further improved by adding:

* Interactive dashboards using **Power BI** or **Tableau**.
* More detailed city-level funding analysis.
* Monthly and quarterly funding trends.
* Funding amount conversion into USD.
* Investor-to-startup network analysis.
* Startup survival or success analysis if additional data is available.
* Statistical correlation analysis between numerical variables.
* More robust investor-type classification.
* Automated data-cleaning pipelines.
* Interactive Plotly visualizations.
* Machine-learning models for funding prediction.

---

## 👨‍💻 Skills Demonstrated

This project demonstrates practical experience in:

* Data Cleaning
* Exploratory Data Analysis (EDA)
* Data Preprocessing
* Pandas
* NumPy
* Data Visualization
* Statistical Analysis
* GroupBy & Aggregation
* Cross-tabulation
* Outlier Detection
* Trend Analysis
* Investor Classification
* Business Insight Generation

---

## 📌 Conclusion

The **Indian Startups Funding Analysis** project provides an exploratory view of India's startup funding ecosystem using historical funding data.

By analyzing funding trends, sectors, investors, investment types, outliers, growth patterns, and startup trajectories, the project demonstrates how Python-based data analytics can be used to transform raw startup funding data into meaningful business insights.

---

## 📜 License

This project is intended for **educational and portfolio purposes**.

If the dataset is obtained from a third-party source, please follow the original dataset's terms and licensing requirements.
