# Quality & Coverage Assessment Report

This document summarizes data quality checks performed on the cleaned Ames Housing dataset.

## 1. Missingness per Column
All values should be 0% after cleaning.

```
PID                 0.000000
Fireplace Qu        0.000000
Fireplaces          0.000000
Functional          0.000000
TotRms AbvGrd       0.000000
Kitchen Qual        0.000000
Kitchen AbvGr       0.000000
Bedroom AbvGr       0.000000
Garage Type         0.000000
Half Bath           0.000000
Bsmt Half Bath      0.000000
Bsmt Full Bath      0.000000
Gr Liv Area         0.000000
Low Qual Fin SF     0.000000
2nd Flr SF          0.000000
1st Flr SF          0.000000
Electrical          0.000000
Full Bath           0.000000
Central Air         0.000000
Garage Yr Blt       0.000000
Garage Cars         0.000000
Sale Type           0.000000
Yr Sold             0.000000
Mo Sold             0.000000
Misc Val            0.000000
Fence               0.000000
Pool QC             0.000000
Pool Area           0.000000
Garage Finish       0.000000
Screen Porch        0.000000
Enclosed Porch      0.000000
Open Porch SF       0.000000
Wood Deck SF        0.000000
Paved Drive         0.000000
Garage Cond         0.000000
Garage Qual         0.000000
Garage Area         0.000000
3Ssn Porch          0.000000
Sale Condition      0.000000
Heating QC          0.000000
Total Bsmt SF       0.000000
Overall Qual        0.000000
House Style         0.000000
Bldg Type           0.000000
Condition 2         0.000000
Condition 1         0.000000
Neighborhood        0.000000
Land Slope          0.000000
Heating             0.000000
Lot Config          0.000000
Land Contour        0.000000
Lot Shape           0.000000
Street              0.000000
Lot Area            0.000000
Lot Frontage        0.000000
MS Zoning           0.000000
MS SubClass         0.000000
Utilities           0.000000
Year Built          0.000000
Overall Cond        0.000000
Roof Style          0.000000
Bsmt Unf SF         0.000000
BsmtFin SF 2        0.000000
BsmtFin Type 2      0.000000
BsmtFin SF 1        0.000000
BsmtFin Type 1      0.000000
Bsmt Exposure       0.000000
Year Remod/Add      0.000000
Bsmt Qual           0.000000
Bsmt Cond           0.000000
Exter Cond          0.000000
Exter Qual          0.000000
Mas Vnr Area        0.000000
Exterior 2nd        0.000000
Exterior 1st        0.000000
Roof Matl           0.000000
Foundation          0.000000
SalePrice           0.000000
Mas Vnr Type       60.580205
Alley              93.242321
Misc Feature       96.382253
```

## 2. Low-Variability Columns (≤ 2 unique values)
```
['Street', 'Alley', 'Central Air', 'Fence']
```

## 3. Dominant Categories (>85%)
| Column | Category | Percentage |
|--------|----------|------------|
| Street | Pave | 99.6% |
| Land Contour | Lvl | 89.9% |
| Utilities | AllPub | 99.9% |
| Land Slope | Gtl | 95.2% |
| Condition 1 | Norm | 86.1% |
| Condition 2 | Norm | 99.0% |
| Roof Matl | CompShg | 98.5% |
| Heating | GasA | 98.5% |
| Central Air | Y | 93.3% |
| Electrical | SBrkr | 91.6% |
| Paved Drive | Y | 90.5% |
| Misc Feature | Shed | 89.6% |
| Sale Type | WD | 86.6% |

## 4. Rare Categories (<1%)
- **MS Zoning**: ['RH', 'C (all)', 'I (all)', 'A (agr)']
- **Street**: ['Grvl']
- **Lot Shape**: ['IR3']
- **Utilities**: ['NoSewr', 'NoSeWa']
- **Lot Config**: ['FR3']
- **Land Slope**: ['Sev']
- **Neighborhood**: ['Blmngtn', 'Veenker', 'NPkVill', 'Blueste', 'Greens', 'GrnHill', 'Landmrk']
- **Condition 1**: ['RRAe', 'PosA', 'RRNn', 'RRNe']
- **Condition 2**: ['Feedr', 'Artery', 'PosA', 'PosN', 'RRNn', 'RRAe', 'RRAn']
- **House Style**: ['2.5Unf', '1.5Unf', '2.5Fin']
- **Year Built**: ['1900-01-01', '1969-01-01', '1992-01-01', '1980-01-01', '1948-01-01', '1930-01-01', '1975-01-01', '2009-01-01', '1953-01-01', '1915-01-01', '1941-01-01', '1974-01-01', '1979-01-01', '1973-01-01', '1939-01-01', '1926-01-01', '1990-01-01', '1984-01-01', '1949-01-01', '1952-01-01', '1951-01-01', '1923-01-01', '1924-01-01', '1922-01-01', '1946-01-01', '1988-01-01', '1945-01-01', '1935-01-01', '1938-01-01', '1991-01-01', '1936-01-01', '1921-01-01', '1947-01-01', '1986-01-01', '1916-01-01', '1981-01-01', '1918-01-01', '1937-01-01', '1928-01-01', '1927-01-01', '1987-01-01', '1983-01-01', '1914-01-01', '1929-01-01', '1989-01-01', '1982-01-01', '1931-01-01', '1985-01-01', '1890-01-01', '1942-01-01', '1934-01-01', '1932-01-01', '1912-01-01', '1880-01-01', '1919-01-01', '1905-01-01', '2010-01-01', '1917-01-01', '1895-01-01', '1885-01-01', '1908-01-01', '1892-01-01', '1901-01-01', '1893-01-01', '1879-01-01', '1906-01-01', '1911-01-01', '1896-01-01', '1872-01-01', '1904-01-01', '1902-01-01', '1882-01-01', '1898-01-01', '1907-01-01', '1875-01-01', '1913-01-01']
- **Year Remod/Add**: ['1991-01-01', '1960-01-01', '1990-01-01', '1954-01-01', '1965-01-01', '1966-01-01', '1962-01-01', '1964-01-01', '1969-01-01', '1955-01-01', '1979-01-01', '1961-01-01', '1973-01-01', '1957-01-01', '1953-01-01', '1984-01-01', '1974-01-01', '1989-01-01', '1987-01-01', '1952-01-01', '1988-01-01', '1985-01-01', '1951-01-01', '1986-01-01', '1981-01-01', '2010-01-01', '1983-01-01', '1982-01-01']
- **Roof Style**: ['Gambrel', 'Flat', 'Mansard', 'Shed']
- **Roof Matl**: ['Tar&Grv', 'WdShake', 'WdShngl', 'Membran', 'ClyTile', 'Roll', 'Metal']
- **Exterior 1st**: ['BrkComm', 'AsphShn', 'CBlock', 'Stone', 'PreCast', 'ImStucc']
- **Exterior 2nd**: ['Brk Cmn', 'ImStucc', 'Stone', 'AsphShn', 'CBlock', 'PreCast', 'Other']
- **Mas Vnr Type**: ['CBlock']
- **Foundation**: ['Stone', 'Wood']
- **Heating**: ['GasW', 'Grav', 'Wall', 'OthW', 'Floor']
- **Electrical**: ['FuseP', 'Mix']
- **Garage Type**: ['2Types', 'CarPort']
- **Garage Yr Blt**: ['1973-01-01', '2009-01-01', '1972-01-01', '1971-01-01', '1992-01-01', '1990-01-01', '1953-01-01', '1910-01-01', '1939-01-01', '1988-01-01', '1987-01-01', '1984-01-01', '1989-01-01', '1948-01-01', '1985-01-01', '1925-01-01', '1991-01-01', '1951-01-01', '1952-01-01', '1981-01-01', '1941-01-01', '1926-01-01', '1949-01-01', '1946-01-01', '1922-01-01', '1945-01-01', '1986-01-01', '1938-01-01', '1983-01-01', '1923-01-01', '1935-01-01', '1924-01-01', '1915-01-01', '1982-01-01', '1900-01-01', '1947-01-01', '1916-01-01', '1936-01-01', '1928-01-01', '1942-01-01', '1914-01-01', '1937-01-01', '1931-01-01', '1921-01-01', '1927-01-01', '2010-01-01', '1934-01-01', '1918-01-01', '1932-01-01', '1895-01-01', '1919-01-01', '1912-01-01', '1929-01-01', '1917-01-01', '1890-01-01', '1933-01-01', '1908-01-01', '2207-01-01', '1911-01-01', '1896-01-01', '1906-01-01', '1872-01-01', '1905-01-01', '1902-01-01', '1907-01-01', '1875-01-01', '1943-01-01']
- **Misc Feature**: ['Elev', 'TenC']
- **Sale Type**: ['ConLD', 'CWD', 'ConLI', 'ConLw', 'Oth', 'Con', 'VWD']
- **Sale Condition**: ['Alloca', 'AdjLand']

## 5. Outlier Summary (IQR Method)
Top variables with most outliers:

```
Enclosed Porch    459
BsmtFin Type 2    431
Exter Cond        381
BsmtFin SF 2      351
Garage Qual       315
Bsmt Cond         314
Bsmt Exposure     284
Garage Cond       265
Screen Porch      256
Overall Cond      252
MS SubClass       208
Lot Frontage      206
Mas Vnr Area      203
Functional        202
Bsmt Half Bath    175
```

Variables with zero outliers:

```
['Fence', 'Mo Sold', 'Fireplace Qu', 'Exter Qual', 'BsmtFin Type 1', 'Heating QC', 'Half Bath', 'PID']
```
