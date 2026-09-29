# Exploratory Data Analysis on Adult Income Dataset

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on the Adult Income dataset. The main objective is to understand the dataset, perform data cleaning, analyze numerical and categorical variables, identify missing values and outliers, and visualize important patterns in the data.

The analysis focuses mainly on factors such as **Age, Education, Occupation, Race, Relationship, Income, and Hours per Week**.

---

## 🎯 Objectives

* Understand the structure of the dataset.
* Explore rows, columns, size, and statistical information.
* Analyze categorical and numerical variables.
* Calculate statistical measures such as mean, median, minimum, maximum, and standard deviation.
* Analyze income categories.
* Identify and handle missing values.
* Apply different missing-value handling techniques.
* Detect outliers using IQR and Z-Score methods.
* Apply trimming and winsorization techniques.
* Create different data visualizations.
* Generate automated visualizations using AutoViz.

---

## 📂 Dataset

The project uses the **Adult Income Dataset (`adult.csv`)**.

The dataset contains demographic and employment-related information, including:

* Age
* Workclass
* Education
* Occupation
* Race
* Relationship
* Hours per Week
* Native Country
* Income

The `Income` column represents the income category of an individual.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data loading, manipulation, cleaning, and analysis
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **SciPy** – Z-Score and Winsorization
* **AutoViz** – Automated exploratory data visualization
* **Jupyter Notebook** – Development environment

---

## 🔍 Exploratory Data Analysis

The project performs several EDA operations, including:

### Basic Dataset Exploration

* Display first and last records
* Check dataset shape
* Check dataset size
* Display column names
* Check data types and information
* Generate descriptive statistics
* Count non-null values

Example operations:

```python
df.head()
df.tail()
df.shape
df.size
df.columns
df.describe()
```

---

## 📊 Data Analysis

The project analyzes different aspects of the dataset, including:

* Age distribution
* Education categories
* Occupation
* Income distribution
* Hours worked per week
* Relationship and race information
* Average working hours for different income categories
* Correlation between numerical variables
* Unique values and frequency counts

Statistical measures such as:

* Mean
* Median
* Minimum
* Maximum
* Standard deviation
* Correlation

are also calculated.

---

## 🧹 Data Cleaning

Missing values are identified using the `?` representation in the dataset.

The project demonstrates multiple techniques for handling missing values:

### 1. Replace Missing Values

```python
df = df.replace(" ?", None)
```

### 2. Fill with Constant Values

```python
df.fillna()
```

### 3. Mean Imputation

```python
df["Age"] = df["Age"].fillna(df["Age"].mean())
```

### 4. Median Imputation

```python
df["Age"] = df["Age"].fillna(df["Age"].median())
```

### 5. Mode Imputation

Mode is used for categorical data such as occupation.

### 6. Removing Missing Records

```python
df.dropna()
```

### 7. Forward Filling

```python
df.ffill()
```

### 8. Backward Filling

```python
df.bfill()
```

The notebook also demonstrates interpolation as another missing-value handling technique.

---

## 🚨 Outlier Detection

Outliers are analyzed using two major methods.

### IQR Method

The Interquartile Range is calculated as:

```text
IQR = Q3 - Q1
```

The lower and upper bounds are calculated using:

```text
Lower Bound = Q1 - 1.5 × IQR
Upper Bound = Q3 + 1.5 × IQR
```

The project applies the IQR method to:

* Age
* Hours per Week

### Z-Score Method

Z-Scores are calculated using SciPy:

```python
from scipy.stats import zscore
```

Values with an absolute Z-Score greater than 3 are identified as potential outliers.

---

## ✂️ Outlier Treatment

The notebook demonstrates:

### Z-Score Trimming

Records with Z-Scores outside the selected range are removed.

### Winsorization

Winsorization is demonstrated using:

```python
from scipy.stats.mstats import winsorize
```

This technique limits extreme values instead of completely removing the records.

---

## 📈 Data Visualization

Several visualizations are created using Seaborn and Matplotlib.

### 1. Income Distribution

A count plot is used to understand the number of people in each income category.

### 2. Age Distribution

A histogram is used to analyze the distribution of age.

### 3. Age vs Hours per Week

A scatter plot is used to observe the relationship between age and working hours.

### 4. Hours per Week vs Income

A box plot is used to compare working hours across income categories.

### 5. Average Hours Worked by Income

A bar chart compares the average working hours for different income groups.

---

## 🤖 Automated EDA with AutoViz

The project also uses **AutoViz** to automatically generate visualizations.

Installation:

```python
pip install autoviz
```

AutoViz is used with the `Income` column as the dependent variable.

The notebook demonstrates different chart formats:

```python
chart_format="png"
```

and

```python
chart_format="html"
```

---

## 📁 Project Structure

```text
EDA-Project/
│
├── EDAproject_1.ipynb
├── adult.csv
└── README.md
```

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

### 2. Install required libraries

```bash
pip install pandas matplotlib seaborn scipy autoviz
```

### 3. Open the Jupyter Notebook

```bash
jupyter notebook
```

### 4. Open

```text
EDAproject_1.ipynb
```

### 5. Make sure `adult.csv` is available in the required location.

### 6. Run the notebook cells sequentially.

---

## 📌 Key Analysis Areas

| Area                 | Techniques Used                                                 |
| -------------------- | --------------------------------------------------------------- |
| Data Understanding   | `head()`, `tail()`, `info()`, `shape`, `size`                   |
| Statistics           | Mean, Median, Min, Max, Standard Deviation                      |
| Categorical Analysis | `unique()`, `value_counts()`, `mode()`                          |
| Missing Values       | Mean, Median, Mode, Constant, Drop, Forward Fill, Backward Fill |
| Outliers             | IQR, Z-Score                                                    |
| Outlier Treatment    | Trimming, Winsorization                                         |
| Visualization        | Histogram, Count Plot, Scatter Plot, Box Plot, Bar Chart        |
| Automated EDA        | AutoViz                                                         |

---

## 📌 Conclusion

This project demonstrates a complete **Exploratory Data Analysis workflow** using the Adult Income dataset. It covers data understanding, statistical analysis, data cleaning, missing-value treatment, outlier detection, outlier treatment, and data visualization.

The project helps identify patterns and relationships among demographic, educational, employment, and income-related variables and provides a foundation for further statistical analysis or machine learning tasks.

---

## 👩‍💻 Author

**Shalini**

B.Tech Final Year Student

**GitHub:** https://github.com/shalini2705
