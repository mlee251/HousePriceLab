# Quality & Coverage Assessment Report

This document summarizes data quality checks performed on the cleaned Ames Housing dataset.

## 1. Missingness per Column
All values should be 0% after cleaning.

```
PID                0.0
Fireplace Qu       0.0
Fireplaces         0.0
Functional         0.0
TotRms AbvGrd      0.0
Kitchen Qual       0.0
Kitchen AbvGr      0.0
Bedroom AbvGr      0.0
Garage Type        0.0
Half Bath          0.0
Bsmt Half Bath     0.0
Bsmt Full Bath     0.0
Gr Liv Area        0.0
Low Qual Fin SF    0.0
2nd Flr SF         0.0
1st Flr SF         0.0
Electrical         0.0
Full Bath          0.0
Garage Yr Blt      0.0
Garage Finish      0.0
Garage Cars        0.0
Sale Type          0.0
Yr Sold            0.0
Mo Sold            0.0
Misc Val           0.0
Misc Feature       0.0
Fence              0.0
Pool QC            0.0
Pool Area          0.0
Screen Porch       0.0
3Ssn Porch         0.0
Enclosed Porch     0.0
Open Porch SF      0.0
Wood Deck SF       0.0
Paved Drive        0.0
Garage Cond        0.0
Garage Qual        0.0
Garage Area        0.0
Central Air        0.0
Sale Condition     0.0
Heating QC         0.0
Total Bsmt SF      0.0
House Style        0.0
Bldg Type          0.0
Condition 2        0.0
Condition 1        0.0
Neighborhood       0.0
Land Slope         0.0
Lot Config         0.0
Overall Qual       0.0
Utilities          0.0
Lot Shape          0.0
Alley              0.0
Street             0.0
Lot Area           0.0
Lot Frontage       0.0
MS Zoning          0.0
MS SubClass        0.0
Land Contour       0.0
Overall Cond       0.0
Year Built         0.0
Year Remod/Add     0.0
Bsmt Unf SF        0.0
BsmtFin SF 2       0.0
BsmtFin Type 2     0.0
BsmtFin SF 1       0.0
BsmtFin Type 1     0.0
Bsmt Exposure      0.0
Bsmt Cond          0.0
Bsmt Qual          0.0
Foundation         0.0
Exter Cond         0.0
Exter Qual         0.0
Mas Vnr Area       0.0
Mas Vnr Type       0.0
Exterior 2nd       0.0
Exterior 1st       0.0
Roof Matl          0.0
Roof Style         0.0
Heating            0.0
SalePrice          0.0
```

## 2. Low-Variability Columns (≤ 2 unique values)
```
['Street', 'Central Air', 'Fence']
```

## 3. Dominant Categories (>85%)
| Column | Category | Percentage |
|--------|----------|------------|
| Street | Pave | 99.6% |
| Alley | None | 93.2% |
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
| Misc Feature | None | 96.4% |
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
- **Mas Vnr Type**: ['BrkCmn', 'CBlock']
- **Foundation**: ['Stone', 'Wood']
- **Heating**: ['GasW', 'Grav', 'Wall', 'OthW', 'Floor']
- **Electrical**: ['FuseP', 'Mix']
- **Garage Type**: ['2Types', 'CarPort']
- **Garage Yr Blt**: ['1973-01-01', '2009-01-01', '1972-01-01', '1971-01-01', '1992-01-01', '1990-01-01', '1953-01-01', '1910-01-01', '1939-01-01', '1988-01-01', '1987-01-01', '1984-01-01', '1989-01-01', '1948-01-01', '1985-01-01', '1925-01-01', '1991-01-01', '1951-01-01', '1952-01-01', '1981-01-01', '1941-01-01', '1926-01-01', '1949-01-01', '1946-01-01', '1922-01-01', '1945-01-01', '1986-01-01', '1938-01-01', '1983-01-01', '1923-01-01', '1935-01-01', '1924-01-01', '1915-01-01', '1982-01-01', '1900-01-01', '1947-01-01', '1916-01-01', '1936-01-01', '1928-01-01', '1942-01-01', '1914-01-01', '1937-01-01', '1931-01-01', '1921-01-01', '1927-01-01', '2010-01-01', '1934-01-01', '1918-01-01', '1932-01-01', '1895-01-01', '1919-01-01', '1912-01-01', '1929-01-01', '1917-01-01', '1890-01-01', '1933-01-01', '1908-01-01', '2207-01-01', '1911-01-01', '1896-01-01', '1906-01-01', '1872-01-01', '1905-01-01', '1902-01-01', '1907-01-01', '1875-01-01', '1943-01-01']
- **Misc Feature**: ['Gar2', 'Othr', 'Elev', 'TenC']
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
