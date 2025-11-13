# 🚕 Uber Rideshare Data Analysis & Optimization

This project conducts a comprehensive **Exploratory Data Analysis (EDA)** on personal 2016 Uber trip data to uncover underlying user driving habits, identify peak usage trends, and evaluate factors that influence trip efficiency. The analysis focuses on temporal patterns, geographic origins, destinations, and the stated purpose of each ride.

---

## 🎯 Project Goal

The primary objective is to analyze the trip data to better understand **personal mobility habits** and diagnose areas for potential **trip efficiency optimization**.

### Key Questions Addressed

1. How has trip activity changed over time (Time Series)?  
2. What are the most common starting and ending points (Geospatial Analysis)?  
3. What is the distribution of trip purposes and travel distances?  
4. How does the length of a trip relate to its purpose?

---

## 📁 Data Source and Preprocessing

The analysis is performed on a dataset of Uber drives from 2016.

- **File:** `My Uber Drives - 2016.csv`  
- **Data Cleaning:** Missing values in the `PURPOSE*` column were imputed with `"NOT"`.  
  Remaining rows with missing data were dropped, resulting in a cleaned dataset of **1,136 trips**.

### 🧮 Feature Engineering

A critical step involved transforming the raw date and time fields into actionable temporal features:

- `START_DATE*` and `END_DATE*` columns were converted to `datetime` objects.  
- New features were created:
  - **`Date`** and **`Time`** (hour of the day) extracted from `START_DATE*`.  
  - **`Day/Night`** segmented into four categories: Morning, Afternoon, Evening, and Night.

---

## 🛠️ Technologies & Skills

The project is built entirely within a **Jupyter Notebook** environment, leveraging fundamental **data science libraries** in Python.

- **Data Manipulation:** `pandas`  
- **Visualization:** `matplotlib.pyplot`, `seaborn`  
- **Skills:** Exploratory Data Analysis (EDA), `datetime` feature engineering

---

## 💡 Key Findings and Recommendations

The analysis explores trip patterns across time, distance, and purpose to diagnose usage habits. Based on the uncovered trends, the following optimization strategies are recommended:

### 1. **Peak Hour Optimization**

- **Recommendation:** Since trips peak around evening commute hours, explore **shared ride/pool options** during this time to reduce cost.  
- **Goal:** Decrease average trip cost/time by approximately **15%** during peak usage.

---

### 2. **Long-Distance Strategy Review**

- **Recommendation:** For high-mileage trips categorized as **Commute**, evaluate if alternative modes of transport, such as **scheduled public transit or personal driving**, would be more cost-effective.

---

### 3. **Data Quality Improvement**

- **Recommendation:** In future data collection, efforts should be made to minimize the number of trips recorded with an **"Unknown"** purpose to enable richer, more accurate segmentation of driving habits.

---

## 🚀 How to Run the Project

1. **Clone the repository:**
    ```bash
    git clone [your-repo-link]
    ```
2. **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn
    ```
3. **Add the dataset:**
    Ensure the `My Uber Drives - 2016.csv` file is in the root directory.
4. **Run the notebook:**
    Open the `Uber_Data_Analysis.ipynb` file in a Jupyter environment (e.g., JupyterLab, VS Code, Google Colab) and execute the cells sequentially.

---

## 🧾 Author & Acknowledgment

Developed with ❤️ using Python and open-source data visualization tools.  
Dataset sourced from personal Uber drive records (2016).

---
