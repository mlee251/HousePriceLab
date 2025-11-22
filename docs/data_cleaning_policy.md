# Data Cleaning & Standardization Policy

This document defines the cleaning and standardization rules applied to the Ames Housing dataset in this project.  
All transformations are deterministic and driven by semantic groups (ID, temporal, numeric, ordinal, nominal).

---

## 1. ID Columns

**Columns:**
- `Order`
- `PID`

**Policy:**

- `Order`  
  - Meaning: purely a row index from the original dataset.  
  - Action: **drop** (not used for analysis or modeling).

- `PID`  
  - Meaning: parcel (property) identifier.  
  - Action: **keep** as an identifier (not used as a feature, but may be used for joins or traceability).

---

## 2. Temporal Columns

**Columns:**
- `Year Built`
- `Year Remod/Add`
- `Garage Yr Blt`
- `Yr Sold`

**Representation:**

- All temporal variables are stored as **dates** (`datetime64`) instead of plain integers.
- Convention: we map years to dates using **January 1st** of the corresponding year:  
  - Example: `Year Built = 1998` → `1998-01-01`.

**Missing Values:**

- `Garage Yr Blt`:
  - Rule chosen: **Option A**  
  - If `Garage Yr Blt` is missing, set it equal to the house’s `Year Built` before converting to date.
- Other temporal columns:
  - No missing values in the raw dataset; if any appear later, they will be treated as genuine `NaT` (missing datetime).

**Validation:**

- `Year Built` should be in a reasonable range (e.g., 1870–2010).  
- `Yr Sold` should be in [2006, 2010].  
- Any values outside expected ranges will be flagged for manual inspection.

---

## 3. Numeric Continuous Variables

**Examples:**
- `Lot Frontage`, `Lot Area`, `Mas Vnr Area`,  
  `BsmtFin SF 1`, `BsmtFin SF 2`, `Bsmt Unf SF`, `Total Bsmt SF`,  
  `1st Flr SF`, `2nd Flr SF`, `Low Qual Fin SF`, `Gr Liv Area`,  
  `Garage Area`, `Wood Deck SF`, `Open Porch SF`, `Enclosed Porch`,  
  `3Ssn Porch`, `Screen Porch`, `Pool Area`, `Misc Val`, `SalePrice`.

**Data Types:**

- Stored as numeric (`int64` or `float64`), using integers when values are naturally integer counts (e.g. square feet).

**Missing Values:**

- General rule: **Option A (recommended)**  
  - For continuous variables with small amounts of missing values: impute using the **global median** of that variable.

- Special case: `Lot Frontage`  
  - Missing ≈ 16–17%.  
  - Rule: **median by neighborhood**  
    - For each `Neighborhood`, compute the median `Lot Frontage`.  
    - Impute missing `Lot Frontage` with the median of its neighborhood.  
    - If a neighborhood has all values missing (unlikely), fall back to the global median.

**Outliers & Impossible Values:**

- Negative values for areas or frontages are considered **invalid** and will be flagged.  
- We will not remove outliers at this stage; they will be:
  - Detected and documented.
  - Possibly treated or winsorized later at the modeling stage if needed.

---

## 4. Numeric Discrete Variables

**Examples:**
- `Bsmt Full Bath`, `Bsmt Half Bath`, `Full Bath`, `Half Bath`,  
  `Bedroom AbvGr`, `Kitchen AbvGr`, `TotRms AbvGrd`, `Fireplaces`, `Garage Cars`.

**Data Types:**

- Stored as **integers** (`int64`).
- Any float types arising from missing values will be converted to integers after imputation.

**Missing Values:**

- Rule: **Option A (mode imputation)**  
  - For each discrete numeric variable, replace missing values with the **most frequent value** (mode) in that column.
  - Interpretation: missing is treated as “typical” behavior for that feature.

**Validation:**

- Negative counts are invalid and will be flagged.  
- For each variable, the allowed range is checked, e.g.:  
  - `Full Bath` in {0, 1, 2, 3, 4}  
  - `Kitchen AbvGr` typically in {0, 1, 2, 3}.

---

## 5. Categorical Ordinal Variables

**Examples:**
- `Overall Qual`, `Overall Cond`,  
  `Exter Qual`, `Exter Cond`,  
  `Bsmt Qual`, `Bsmt Cond`, `Bsmt Exposure`,  
  `BsmtFin Type 1`, `BsmtFin Type 2`,  
  `Heating QC`, `Kitchen Qual`, `Fireplace Qu`,  
  `Garage Qual`, `Garage Cond`,  
  `Pool QC`, `Fence`, `Functional`.

**Representation:**

- Ordinal variables keep their semantic order and are encoded as **integers**.
- Example mappings (to be implemented explicitly in code):

  - Quality scales (e.g., `Exter Qual`, `Kitchen Qual`, etc.):
    - `NA` (no feature) → 0  
    - `Po` → 1  
    - `Fa` → 2  
    - `TA` → 3  
    - `Gd` → 4  
    - `Ex` → 5  

  - Exposure (e.g., `Bsmt Exposure`):
    - `NA` → 0  
    - `No` → 1  
    - `Mn` → 2  
    - `Av` → 3  
    - `Gd` → 4  

  - Functional:
    - `Sal` (salvage) → 1  
    - `Sev` → 2  
    - `Maj2` → 3  
    - `Maj1` → 4  
    - `Mod` → 5  
    - `Min2` → 6  
    - `Min1` → 7  
    - `Typ` → 8  

  - Basement finish types (`BsmtFin Type 1/2`):
    - `NA` → 0  
    - `Unf` → 1  
    - `LwQ` → 2  
    - `Rec` → 3  
    - `BLQ` → 4  
    - `ALQ` → 5  
    - `GLQ` → 6  

**Missing Values:**

- General rule:  
  - If missing means **absence of feature** (e.g. no basement, no fireplace, no pool, no fence), treat missing as a **special lowest category**:
    - e.g. map missing → `"NA"` → numeric value `0`.

- This preserves:

  - The ordinal nature of the variable.
  - The information that the feature is absent.

---

## 6. Categorical Nominal Variables

**Examples:**
- `MS SubClass`, `MS Zoning`, `Street`, `Alley`, `Lot Shape`, `Land Contour`,  
  `Utilities`, `Lot Config`, `Land Slope`, `Neighborhood`,  
  `Condition 1`, `Condition 2`, `Bldg Type`, `House Style`,  
  `Roof Style`, `Roof Matl`, `Exterior 1st`, `Exterior 2nd`,  
  `Mas Vnr Type`, `Foundation`, `Heating`, `Central Air`, `Electrical`,  
  `Garage Type`, `Garage Finish`, `Paved Drive`, `Misc Feature`,  
  `Sale Type`, `Sale Condition`, `Mo Sold`.

**Text Standardization:**

- Strip leading/trailing whitespace from all categories.  
- Preserve original casing as used in documentation (no forced lowercasing unless necessary).

**Missing Values:**

- Variables where missing means **“no such feature”**:
  - `Alley`, `Fireplace Qu`, `Pool QC`, `Fence`, `Misc Feature`, some basement-related fields when appropriate.

  - Rule:  
    - Impute missing with the category `"None"` (or equivalent, e.g. `"NoAlley"`, `"NoPool"`).  
    - This creates an explicit category for absence of the feature.

- Variables where missing means **“not recorded”** (rare):
  - Example: `Electrical` (single missing).  
  - Rule:  
    - Impute with the **mode** (most frequent category).

**Encoding for Modeling:**

- For ML models that require numeric inputs, nominal categories will later be encoded using:
  - One-hot encoding, or
  - Target/frequency encoding (depending on the model and experiment),  
  but that is part of the **modeling** phase, not the cleaning phase.

---

## 7. Summary of Key Design Choices

- **Order**: dropped.  
- **PID**: kept as an identifier, not used as a feature.
- **Temporal variables**: converted to `datetime` using January 1st of each year; missing `Garage Yr Blt` → `Year Built`.
- **Numeric continuous**: missing values imputed using medians (global), with `Lot Frontage` imputed by neighborhood median.
- **Numeric discrete**: missing values imputed using the mode.
- **Ordinal categorical**: mapped to ordered integers, with missing mapped to `NA`/0 when representing absence of the feature.
- **Nominal categorical**: cleaned strings; missing as `"None"` when absence is meaningful, otherwise imputed with the mode.

These rules will be implemented in a single, reproducible cleaning pipeline so that anyone can reproduce the cleaned dataset from the original raw file.