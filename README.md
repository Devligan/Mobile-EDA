# 📊 Mobile Phone Dataset EDA

This notebook contains an exploratory data analysis (EDA) of a mobile phone dataset, aiming to understand the relationship between various hardware/software features and the price of the devices.

---

## 📁 Dataset Overview

The dataset contains specifications for mobile phones such as:
- Hardware features: RAM, storage, battery, camera, etc.
- Connectivity: 3G/4G/5G, NFC, IR blaster, Wi-Fi, etc.
- Display and build: screen size, refresh rate, resolution, protection
- Brand, model, and launch details
- Target variable: `price_usd`

---

## 🧹 Data Cleaning

- Standardized missing values and filled them where appropriate
- Converted all text columns to lowercase for consistency
- Extracted and converted:
  - RAM and storage sizes into numeric GB values
  - Battery capacity and charging speeds
  - External memory support with size normalization (TB → GB)
- Removed outliers and unrealistic values in price and spec score

---

## 📊 Exploratory Data Analysis

### 🔢 Distribution Analysis
- Histograms and KDE plots for key numerical features (price, RAM, battery, etc.)
- Count plots for categorical and binary features (brand, dual SIM, NFC, etc.)

### 🔍 Feature Relationships
- Scatterplots of `price_usd` vs. features such as `spec score`, `battery`, and `RAM`
- Polynomial trend line (degree 9) fitted to `price_usd` vs. `spec score`

### 🧪 Correlation Analysis
- Pearson correlation heatmap (numeric + encoded categorical features)
- Highlighted top correlated features with price (excluding `price`, `price_usd`)

### 📈 Model Insights (Optional)
- Trained simple regression model (if applicable)
- Plotted actual vs. predicted prices and residual distribution

---

## 🏷️ Feature Engineering

- Created binary flags for:
  - `has_fast_charging`, `has_ir_blaster`, `has_5g`, etc.
- Encoded categorical variables with `LabelEncoder`
- Derived `external_memory_gb` and `external_memory_supported`

---

## 📌 Key Findings

- `spec score`, `brand`, `5G`, and `fast charging` are strongly correlated with price
- Several SIM and connectivity features showed weak or no correlation
- Polynomial regression captures nonlinear relationship between specs and price

---

## 📦 Files

- [`main.ipynb`](https://github.com/Devligan/Mobile_EDA_-_Price_Predictor/blob/main/main.ipynb): Jupyter notebook with full analysis
- [`README.md`](https://github.com/Devligan/Mobile_EDA_-_Price_Predictor/blob/main/README.md): Project overview (this file)

---
