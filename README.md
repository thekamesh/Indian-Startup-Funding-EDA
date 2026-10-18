# 📊 Indian Startup Funding — EDA

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on the **Indian Startup Funding** dataset.

The analysis focuses on understanding startup funding patterns in India by exploring funding amounts, industries, investment types, cities, investors, and funding trends over time.

The project also includes **data cleaning and preprocessing** to make the raw dataset suitable for meaningful analysis and visualization.

---

## 🎯 Objectives

The main objectives of this project are:

- Understand the structure and quality of the dataset
- Identify and handle missing values
- Check for duplicate records
- Clean and standardize column names
- Convert dates into proper datetime format
- Clean and convert funding amounts into numerical values
- Analyze startup funding trends
- Explore funding across different industries
- Analyze investment types
- Identify major startup locations
- Analyze investor participation
- Create meaningful visualizations to identify patterns and trends

---

## 📂 Dataset

The dataset used in this project is the **Indian Startup Funding** dataset.

### Initial Dataset Size

- **Rows:** 3,044
- **Columns:** 10

### Original Columns

- `Sr No`
- `Date dd/mm/yyyy`
- `Startup Name`
- `Industry Vertical`
- `SubVertical`
- `City Location`
- `Investors Name`
- `InvestmentnType`
- `Amount in USD`
- `Remarks`

The dataset contains information about Indian startups, their industries, locations, investors, investment types, and funding amounts.

---

## 🧹 Data Cleaning

Several preprocessing steps were performed before EDA.

### 1. Column Name Standardization

The original column names were renamed to cleaner and easier-to-use names:

```text
Sr_No
Date
Startup_Name
Industry
Sub_Vertical
City
Investors
Investment_Type
Funding_USD
Remarks
```



### 2. Date Cleaning

Several inconsistent date values were corrected and the `Date` column was converted into proper Pandas datetime format.

```python
df['Date'] = pd.to_datetime(df['Date'], format="%d/%m/%Y")
```

This allows proper time-based analysis such as yearly funding trends.

### 3. Handling Missing Values

Missing values were identified across the dataset.

Some of the major missing-value counts in the raw dataset were:

| Column | Missing Values |
|---|---:|
| Industry | 171 |
| SubVertical | 936 |
| City | 180 |
| Investors | 24 |
| Investment Type | 4 |
| Amount in USD | 960 |
| Remarks | 2625 |



The `Remarks` column was removed because it contained a very high proportion of missing values.

After removing it, the dataset contained **9 columns**.

### 4. Funding Amount Cleaning

The `Funding_USD` column originally contained values with commas as well as values such as:

- `undisclosed`
- `unknown`
- missing values

These values were cleaned and prepared for numerical analysis.

### 5. Duplicate Check

Duplicate records were checked using:

```python
df.duplicated().sum()
```

The initial duplicate check returned **0 duplicate records**.

---

## 🔍 Exploratory Data Analysis

The EDA focuses on understanding the Indian startup ecosystem from multiple perspectives.

### 📈 Funding Analysis

Analysis of startup funding includes:

- Funding distribution
- Funding trends over time
- Funding by industry
- Funding by city
- Funding by investment type

### 🏭 Industry Analysis

The project explores:

- Number of startups/funding deals by industry
- Funding distribution across industries
- Major industries receiving startup investment

### 🏙️ City Analysis

The analysis investigates startup activity across different Indian cities, including:

- Number of startups by city
- Funding distribution by city
- Major startup hubs

### 💰 Investment Type Analysis

Different investment types are explored to understand how startups are funded.

Examples include:

- Seed Round
- Series A
- Series B
- Series C
- Private Equity Round
- Pre-series A

The dataset contains **55 unique investment-type values** in the initial data.

### 👥 Investor Analysis

The project also examines investor participation and identifies investors involved in startup funding activities.

---

## 📊 Visualizations

The project uses Python visualization libraries to present the analysis.

### Libraries Used

- **Matplotlib**
- **Seaborn**

The notebook also uses **Pandas** and **NumPy** for data manipulation and numerical analysis.

Visual analysis includes charts for:

- Funding trends
- Industry-wise funding
- City-wise startup activity
- Investment type distribution
- Funding distribution
- Industry vs Funding
- City vs Funding
- Industry × Investment Type relationships
- Year × Industry trends

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming & analysis |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Jupyter Notebook / Google Colab | Development environment |
| KaggleHub | Dataset download |

---

## 📁 Project Structure

```text
Indian-Startup-Funding-EDA/
│
├── Indian_Startup_Funding_EDA_.ipynb
├── README.md
└── startup_funding.csv
```

> The notebook downloads the dataset using KaggleHub, so the CSV file does not necessarily need to be stored inside the repository.

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone <https://github.com/thekamesh/Indian-Startup-Funding-EDA/tree/main>
```

### 2. Open the notebook

Open:

```text
Indian_Startup_Funding_EDA_.ipynb
```

using:

- Jupyter Notebook
- JupyterLab
- Google Colab
- VS Code

### 3. Install required libraries

```bash
pip install pandas numpy matplotlib seaborn kagglehub
```

### 4. Run the notebook

Execute the cells sequentially to reproduce the data cleaning process and EDA.

---

## 📌 Key Dataset Information

The initial dataset contains:

- **3,044 funding records**
- **2,459 unique startup names**
- **821 unique industry values**
- **112 unique cities**
- **2,412 unique investor entries**
- **55 unique investment types**



---

## 📚 What I Learned From This Project

Through this project, I practiced:

- Exploratory Data Analysis
- Data cleaning
- Missing-value analysis
- Duplicate detection
- Data type conversion
- Date preprocessing
- String cleaning
- Numerical data preprocessing
- GroupBy analysis
- Aggregation
- Data visualization
- Trend analysis
- Business-oriented interpretation of data

---

## 🔗 Dataset Source

The dataset is the **Indian Startup Funding** dataset available through Kaggle and is downloaded in the notebook using KaggleHub.

---

## 👨‍💻 Author

**Kamesh Gupta**

This project was created as part of my Data Analysis / EDA learning journey.
