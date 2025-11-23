# Feature Engineering Report — Ames Housing Dataset
Version: v1  
This document summarizes all engineered features produced in `03_feature_engineering.ipynb`.

---

## 1. Overview
This report documents all transformations performed during feature engineering: structural, temporal, ratio, interaction, and log-transformed features.  
Input: `data/cleaned/ames_cleaned.csv`  
Output: `data/features/ames_features.csv`

---

## 2. Structural & Area-Based Features

### Total_Bathrooms
Full Bath + 0.5×Half Bath + Bsmt Full Bath + 0.5×Bsmt Half Bath

### Total_Bsmt_Finished_SF
BsmtFin SF 1 + BsmtFin SF 2

### Total_Porch_SF
Open Porch SF + Enclosed Porch + 3Ssn Porch + Screen Porch

### Total_House_SF
Gr Liv Area + Total_Bsmt_Finished_SF

### Outdoor_SF
Wood Deck SF + Open Porch SF

---

## 3. Age-Based Features
(All temporal fields converted to datetime)

### House_Age
Yr Sold − Year Built

### Since_Remodel
Yr Sold − Year Remod/Add

### Garage_Age
Yr Sold − Garage Yr Blt  
(missing values replaced with Year Built)

---

## 4. Ratio Features
Area_per_Room = Gr Liv Area / TotRms AbvGrd  
Area_per_Bedroom = Gr Liv Area / Bedroom AbvGr  
Bathrooms_per_Bedroom = Total_Bathrooms / Bedroom AbvGr  
Outdoor_to_TotalArea = Outdoor_SF / (Total_House_SF + 1)  
Basement_to_Living_Ratio = Total_Bsmt_Finished_SF / (Gr Liv Area + 1)

---

## 5. Interaction Features
Quality_x_Area = Overall Qual × Gr Liv Area  
Quality_x_TotalSF = Overall Qual × Total_House_SF  
Condition_x_Age = Overall Cond × House_Age  
Rooms_x_Bathrooms = TotRms AbvGrd × Total_Bathrooms  
Bedrooms_x_Bathrooms = Bedroom AbvGr × Total_Bathrooms  
Bsmt_Quality_x_FinishedSF = Bsmt Qual × Total_Bsmt_Finished_SF

---

## 6. Log-Transformed Features
Applied using log1p():

- Lot Area  
- Gr Liv Area  
- Total_House_SF  
- Total_Bsmt_Finished_SF  
- Total_Porch_SF  
- Outdoor_SF  
- SalePrice  

Fixes skewness and improves modeling.

---

## 7. Categorical Encoding Preparation
Ordinal features mapped based on domain meaning.  
Nominal features prepared for one-hot encoding.  
Cardinality recorded for all categorical columns.

---

## 8. Final Output
Final engineered dataset saved to:

End of Report.
