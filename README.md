# MSCS_634 Lab_1: Data Visualization, Preprocessing & Statistical Analysis

### Overview

This lab focuses on applying data analysis techniques using Python in a Jupyter Notebook environment. The dataset used represents retail **sales data** from kaggle available at https://www.kaggle.com/datasets/chadwambles/supermarket-sales?select=sales.csv, including product information, prices, quantities, taxes, and reward points.

The lab is divided into four major steps:
1. Data Collection and Loading
2. Data Visualization
3. Data Preprocessing (Cleaning, Outlier Handling, Reduction, Scaling)
4. Statistical Analysis

---

### Dataset Summary

- **Filename:** `sales.csv`
- **Records:** 1,000
- **Features:** 12 (including categorical and numerical types)
- **Target of Analysis:** `total_price`

---

### Visualizations and Insights

#### 1. **Scatter Plot: Unit Price vs Total Price**
- Showed a **positive linear correlation**, confirming that higher unit prices contribute to higher total prices.
- Products were color-coded by category to show the distribution across types.

#### 2. **Box Plot: Total Price by Product Category**
- Helped in **identifying outliers** and comparing spending behavior across product types.
- Categories such as "Household" and "Personal Care" showed wider price distributions.

---

### Data Preprocessing

#### Missing Values
- No missing values were detected in the dataset.

#### Outlier Detection
- Outliers were detected using **Interquartile Range (IQR)**.
- After removal, the dataset size was reduced from **1000 to 928** records.

#### Data Reduction
- Applied **80% random sampling** to reduce dataset size to **742**.
- Dropped columns: `sale_id`, `customer_type`.

#### Scaling & Discretization
- Applied **Min-Max scaling** on `unit_price`, `quantity`, `tax`, and `total_price`.
- Discretized `unit_price` into 3 bins: `Low`, `Medium`, `High`.

---

### Statistical Summary

#### Central Tendency (for `total_price`)
- **Min:** 1.21
- **Max:** 433.99
- **Mean:** 118.58
- **Median:** 89.70
- **Mode:** 60.67

#### Dispersion Measures
- **Range:** 432.78
- **Q1:** 38.38
- **Q3:** 176.07
- **IQR:** 137.69
- **Variance:** 9987.29
- **Standard Deviation:** 99.94

#### Correlation Matrix Highlights:
- `tax` ↔ `total_price`: **1.0 (perfect correlation)**  
- `quantity` ↔ `total_price`: **0.66**  
- `unit_price` ↔ `total_price`: **0.52**  

---

### Tools Used

- **Pandas**: Data manipulation
- **Seaborn / Matplotlib**: Visualization
- **NumPy**: Numeric operations
- **Scikit-learn**: Scaling
- **Jupyter Notebook**: Development environment

---

### Challenges Faced

- Outlier removal initially affected dataset balance; adjustments made to retain reasonable sample size.
- Ensuring correct scaling without altering the integrity of categorical fields.
- Managing multi-type columns during correlation and preprocessing.

