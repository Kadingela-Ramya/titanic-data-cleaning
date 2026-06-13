# Titanic Data Cleaning and Visualization

## About This Project

I picked the Titanic dataset for this task because it is one of the most
well-known datasets that has real messy data problems like missing values,
outliers, and wrong data types. The main goal was not just to clean the
data but to actually understand what the data is saying and present it
in a visual way.

The question I wanted to answer was simple — who survived the Titanic
and why? That kept the work focused and made the visualizations more
meaningful.

---

## Dataset Used

- Name: Titanic Passenger Dataset
- Source: Loaded directly using Seaborn library (no download needed)
- Total rows: 891 passengers
- Total columns: 15
- Target column: survived (0 = did not survive, 1 = survived)

---

## What I Did

### Step 1 — Looked at the raw data first
Before touching anything I checked the shape, data types, and where
the missing values were. The Age column had around 20% missing data,
the Cabin column had 77% missing, and Embarked had just 2 missing rows.

### Step 2 — Cleaned the data
- Age: filled missing values with the median age which was 28
- Cabin: removed the column completely since 77% was empty and it
  would not add any useful information
- Embarked: filled the 2 missing entries with the most common value
  which was Southampton
- Removed duplicate rows
- Fixed data types for survived and pclass columns

### Step 3 — Handled outliers
The Fare column had some very extreme values going up to 512 pounds.
I used the IQR method to detect these outliers and capped them at a
reasonable upper limit instead of deleting those rows entirely.

### Step 4 — Created visualizations
Made charts to show what the cleaned data was actually saying.

---

## Visualizations Made

- Missing values heatmap to see where the gaps were
- Age distribution before and after filling missing values
- Boxplot of Fare before and after handling outliers
- Survival rate by gender
- Survival rate by passenger class
- Correlation heatmap of all numeric features
- Scatter plot of Age vs Fare colored by survival status

---

## What I Found

- Only 41.3% of passengers survived overall
- Women had a 74% survival rate while men had only 21.5%
- First class passengers survived at 63% vs third class at just 26%
- Gender turned out to be the strongest factor in survival
- Passengers who paid higher fares and were in upper classes had
  much better access to lifeboats

---

## What I Learned

This task taught me that cleaning data is not just about fixing
numbers. Every decision like whether to fill a missing value or
drop a column actually affects what your final analysis looks like.
The visualization part helped me see that data can tell a clear
story if you prepare it properly.

---

## How to Run This

1. Open the notebook file above
2. Click Open in Colab
3. Go to Runtime and click Run All
4. The dataset loads automatically, no need to download anything

---

## Libraries Used

- Pandas
- NumPy
- Matplotlib
- Seaborn
