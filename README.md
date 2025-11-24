# Basic Basket Analysis (2025 Extension)

**Discipline:** Supervised Learning  
**Professor:** Fernando  
**Context:** Extension Work (ICB_2s-2025)

## 👥 Authors
* **Maria Eduarda Sousa Araujo Pompiani Costa**
* **Matheus Rodrigues Gomes**

---

## 📖 Project Overview
This repository contains the analysis and predictive modeling of Basic Basket (*Cesta Básica*) prices. The project utilizes a dataset spanning from 2022 to 2025 to analyze price fluctuations across different supermarkets, focusing on data cleaning, time series analysis, and supervised learning models to predict future prices.

## 📂 Project Structure
* **`extensao2_2025.ipynb`**: The main Jupyter Notebook containing the data ingestion, preprocessing, visualization, and modeling steps.
* **`ICB_2s-2025.xlsx`**: The source dataset (ensure this file is present in the root directory).

---

## ⚙️ Methodology

### 1. Data Cleaning & Preprocessing
To ensure the integrity of the Time Series and Regression models, rigorous preprocessing was applied:
* **Handling Missing Values (Brands):** * *Problem:* The `Marca` (Brand) column contained 6,395 null values.
    * *Solution:* Instead of dropping these rows (which would result in losing valuable price/date data), we filled them with the category `"Sem marca definida"` (Undefined Brand). This treats the absence of a brand as a categorical feature rather than an error.
* **Product Standardization:** * Inconsistent product names were grouped to ensure accurate analysis (e.g., merging "Farinha" into "Farinha de Trigo", and "Pão" into "Pão Francês").
* **Price Per Kilo (PPK) Calculation:**
    * Created a standardized metric `PPK_medio` to allow fair price comparisons between products sold in different package sizes (e.g., 1kg vs. 5kg packages).

### 2. Technologies & Libraries
The project is built using Python and the following key libraries:
* **Data Manipulation:** `pandas`, `numpy`
* **Visualization:** `matplotlib`, `seaborn`
* **Time Series Analysis:** `statsmodels` (Seasonal Decompose, STL, SARIMAX, Adfuller test)
* **Machine Learning:** * `scikit-learn` (RandomForestRegressor, LinearRegression, Metrics)
    * `xgboost` (XGBRegressor)

---

## 🚀 How to Run
1.  Clone this repository.
2.  Ensure you have Python 3.x installed.
3.  Install the required dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn statsmodels scikit-learn xgboost openpyxl
    ```
4.  Place the `ICB_2s-2025.xlsx` file in the same directory as the notebook.
5.  Open and run `extensao2_2025.ipynb`.

---

## 📊 Analysis Goals
The code performs the following major tasks:
1.  **Exploratory Data Analysis (EDA):** Understanding the distribution of prices and quantities.
2.  **Time Series Decomposition:** Analyzing trend, seasonality, and residuals.
3.  **Price Prediction:** Using Supervised Learning algorithms (Random Forest, XGBoost) to forecast future prices based on historical data.
