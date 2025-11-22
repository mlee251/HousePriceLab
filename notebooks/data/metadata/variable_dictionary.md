# Variable Dictionary

This document summarizes all variables in the Ames Housing dataset, including their semantic meaning, type, and basic data profile.

## `Order`

- **Meaning:** Row Order
- **Description:** Row number indicating the observation order in the original dataset.
- **Semantic group:** `id`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 2930
- **Example values:** 1, 2, 3, 4, 5

## `PID`

- **Meaning:** Parcel Identification Number
- **Description:** Unique identifier assigned to each property parcel.
- **Semantic group:** `id`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 2930
- **Example values:** 526301100, 526350040, 526351010, 526353030, 527105010

## `MS SubClass`

- **Meaning:** Building Class
- **Description:** Identifies the type of dwelling (e.g., 1-story, 2-story, split-level).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 16
- **Example values:** 20, 60, 120, 50, 85

## `MS Zoning`

- **Meaning:** Zoning Classification
- **Description:** General zoning classification of the property (e.g., residential, commercial).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 7
- **Example values:** RL, RH, FV, RM, C (all)

## `Lot Frontage`

- **Meaning:** Lot Frontage
- **Description:** Linear feet of street connected to the property.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `float64`
- **Missing values:** 490 (16.724%)
- **Unique values:** 128
- **Example values:** 141.0, 80.0, 81.0, 93.0, 74.0

## `Lot Area`

- **Meaning:** Lot Area
- **Description:** Total square footage of the lot.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 1960
- **Example values:** 31770, 11622, 14267, 11160, 13830

## `Street`

- **Meaning:** Street Type
- **Description:** Type of street access (paved, gravel, etc.).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 2
- **Example values:** Pave, Grvl

## `Alley`

- **Meaning:** Alley Access
- **Description:** Type of alley access to the property.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 2732 (93.242%)
- **Unique values:** 2
- **Example values:** Pave, Grvl

## `Lot Shape`

- **Meaning:** Lot Shape
- **Description:** Overall shape of the property (regular, irregular, etc.).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 4
- **Example values:** IR1, Reg, IR2, IR3

## `Land Contour`

- **Meaning:** Land Contour
- **Description:** Flatness and general contour of the property.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 4
- **Example values:** Lvl, HLS, Bnk, Low

## `Utilities`

- **Meaning:** Utilities
- **Description:** Type of utilities available (gas, electricity, sewage).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 3
- **Example values:** AllPub, NoSewr, NoSeWa

## `Lot Config`

- **Meaning:** Lot Configuration
- **Description:** Property configuration (inside lot, corner lot, cul-de-sac, etc.).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 5
- **Example values:** Corner, Inside, CulDSac, FR2, FR3

## `Land Slope`

- **Meaning:** Land Slope
- **Description:** Slope of the property (gentle, moderate, severe).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 3
- **Example values:** Gtl, Mod, Sev

## `Neighborhood`

- **Meaning:** Neighborhood
- **Description:** Physical location within the city of Ames.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 28
- **Example values:** NAmes, Gilbert, StoneBr, NWAmes, Somerst

## `Condition 1`

- **Meaning:** Primary Proximity Condition
- **Description:** Proximity to main road, railroad, or other environmental factors.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 9
- **Example values:** Norm, Feedr, PosN, RRNe, RRAe

## `Condition 2`

- **Meaning:** Secondary Proximity Condition
- **Description:** Secondary proximity to environmental features.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 8
- **Example values:** Norm, Feedr, PosA, PosN, Artery

## `Bldg Type`

- **Meaning:** Building Type
- **Description:** Type of dwelling (single-family, duplex, townhouse, etc.).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 5
- **Example values:** 1Fam, TwnhsE, Twnhs, Duplex, 2fmCon

## `House Style`

- **Meaning:** House Style
- **Description:** Architectural style of the dwelling (1-story, 2-story, split-level, etc.).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 8
- **Example values:** 1Story, 2Story, 1.5Fin, SFoyer, SLvl

## `Overall Qual`

- **Meaning:** Overall Quality
- **Description:** Overall material and finish quality, rated from 1 (lowest) to 10 (highest).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 10
- **Example values:** 6, 5, 7, 8, 9

## `Overall Cond`

- **Meaning:** Overall Condition
- **Description:** Overall physical condition of the house, rated from 1 (poor) to 10 (excellent).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 9
- **Example values:** 5, 6, 7, 2, 8

## `Year Built`

- **Meaning:** Construction Year
- **Description:** Original construction year of the property.
- **Semantic group:** `temporal`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 118
- **Example values:** 1960, 1961, 1958, 1968, 1997

## `Year Remod/Add`

- **Meaning:** Remodel Year
- **Description:** Year of last remodeling or addition; same as Year Built if no remodeling occurred.
- **Semantic group:** `temporal`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 61
- **Example values:** 1960, 1961, 1958, 1968, 1998

## `Roof Style`

- **Meaning:** Roof Style
- **Description:** Type of roof design (gable, hip, flat, etc.).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 6
- **Example values:** Hip, Gable, Mansard, Gambrel, Shed

## `Roof Matl`

- **Meaning:** Roof Material
- **Description:** Primary roof covering material.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 8
- **Example values:** CompShg, WdShake, Tar&Grv, WdShngl, Membran

## `Exterior 1st`

- **Meaning:** Exterior Covering (Primary)
- **Description:** Primary exterior material covering the house.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 16
- **Example values:** BrkFace, VinylSd, Wd Sdng, CemntBd, HdBoard

## `Exterior 2nd`

- **Meaning:** Exterior Covering (Secondary)
- **Description:** Secondary exterior material (if multiple materials are used).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 17
- **Example values:** Plywood, VinylSd, Wd Sdng, BrkFace, CmentBd

## `Mas Vnr Type`

- **Meaning:** Masonry Veneer Type
- **Description:** Type of masonry veneer applied to the exterior.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 1775 (60.58%)
- **Unique values:** 4
- **Example values:** Stone, BrkFace, BrkCmn, CBlock

## `Mas Vnr Area`

- **Meaning:** Masonry Veneer Area
- **Description:** Area of masonry veneer in square feet.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `float64`
- **Missing values:** 23 (0.785%)
- **Unique values:** 445
- **Example values:** 112.0, 0.0, 108.0, 20.0, 603.0

## `Exter Qual`

- **Meaning:** Exterior Quality
- **Description:** Quality of the material on the exterior (ordinal: Po < Fa < TA < Gd < Ex).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 4
- **Example values:** TA, Gd, Ex, Fa

## `Exter Cond`

- **Meaning:** Exterior Condition
- **Description:** Condition of the exterior material (ordinal scale).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 5
- **Example values:** TA, Gd, Fa, Po, Ex

## `Foundation`

- **Meaning:** Foundation Type
- **Description:** Type of foundation (crawl space, slab, basement, etc.).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 6
- **Example values:** CBlock, PConc, Wood, BrkTil, Slab

## `Bsmt Qual`

- **Meaning:** Basement Quality
- **Description:** Height and quality of the basement (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 80 (2.73%)
- **Unique values:** 5
- **Example values:** TA, Gd, Ex, Fa, Po

## `Bsmt Cond`

- **Meaning:** Basement Condition
- **Description:** Overall condition of the basement (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 80 (2.73%)
- **Unique values:** 5
- **Example values:** Gd, TA, Po, Fa, Ex

## `Bsmt Exposure`

- **Meaning:** Basement Exposure
- **Description:** Walkout or garden-level basement exposure (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 83 (2.833%)
- **Unique values:** 4
- **Example values:** Gd, No, Mn, Av

## `BsmtFin Type 1`

- **Meaning:** Basement Finish Type 1
- **Description:** Primary basement finished area rating (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 80 (2.73%)
- **Unique values:** 6
- **Example values:** BLQ, Rec, ALQ, GLQ, Unf

## `BsmtFin SF 1`

- **Meaning:** Basement Finished Sq Ft 1
- **Description:** Finished square footage of primary basement area.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `float64`
- **Missing values:** 1 (0.034%)
- **Unique values:** 995
- **Example values:** 639.0, 468.0, 923.0, 1065.0, 791.0

## `BsmtFin Type 2`

- **Meaning:** Basement Finish Type 2
- **Description:** Secondary finished area rating (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 81 (2.765%)
- **Unique values:** 6
- **Example values:** Unf, LwQ, BLQ, Rec, GLQ

## `BsmtFin SF 2`

- **Meaning:** Basement Finished Sq Ft 2
- **Description:** Finished square footage of secondary basement area.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `float64`
- **Missing values:** 1 (0.034%)
- **Unique values:** 274
- **Example values:** 0.0, 144.0, 1120.0, 163.0, 168.0

## `Bsmt Unf SF`

- **Meaning:** Basement Unfinished Area
- **Description:** Unfinished square footage of the basement.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `float64`
- **Missing values:** 1 (0.034%)
- **Unique values:** 1137
- **Example values:** 441.0, 270.0, 406.0, 1045.0, 137.0

## `Total Bsmt SF`

- **Meaning:** Total Basement Area
- **Description:** Total square footage of the basement (finished + unfinished).
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `float64`
- **Missing values:** 1 (0.034%)
- **Unique values:** 1058
- **Example values:** 1080.0, 882.0, 1329.0, 2110.0, 928.0

## `Heating`

- **Meaning:** Heating System
- **Description:** Type of heating installed in the property.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 6
- **Example values:** GasA, GasW, Grav, Wall, Floor

## `Heating QC`

- **Meaning:** Heating Quality and Condition
- **Description:** Quality and condition of the heating system (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 5
- **Example values:** Fa, TA, Ex, Gd, Po

## `Central Air`

- **Meaning:** Central Air Conditioning
- **Description:** Whether the house has central AC (Y/N).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 2
- **Example values:** Y, N

## `Electrical`

- **Meaning:** Electrical System
- **Description:** Electrical wiring type.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 1 (0.034%)
- **Unique values:** 5
- **Example values:** SBrkr, FuseA, FuseF, FuseP, Mix

## `1st Flr SF`

- **Meaning:** First Floor Area
- **Description:** Square footage of the first floor.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 1083
- **Example values:** 1656, 896, 1329, 2110, 928

## `2nd Flr SF`

- **Meaning:** Second Floor Area
- **Description:** Square footage of the second floor.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 635
- **Example values:** 0, 701, 678, 776, 892

## `Low Qual Fin SF`

- **Meaning:** Low Quality Finished Area
- **Description:** Finished area of low quality (all floors).
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 36
- **Example values:** 0, 390, 362, 144, 1064

## `Gr Liv Area`

- **Meaning:** Ground Living Area
- **Description:** Above-ground living area in square feet.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 1292
- **Example values:** 1656, 896, 1329, 2110, 1629

## `Bsmt Full Bath`

- **Meaning:** Basement Full Bathrooms
- **Description:** Number of full bathrooms located in the basement.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `float64`
- **Missing values:** 2 (0.068%)
- **Unique values:** 4
- **Example values:** 1.0, 0.0, 2.0, 3.0

## `Bsmt Half Bath`

- **Meaning:** Basement Half Bathrooms
- **Description:** Number of half bathrooms located in the basement.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `float64`
- **Missing values:** 2 (0.068%)
- **Unique values:** 3
- **Example values:** 0.0, 1.0, 2.0

## `Full Bath`

- **Meaning:** Full Bathrooms (Above Grade)
- **Description:** Number of full bathrooms above grade.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 5
- **Example values:** 1, 2, 3, 0, 4

## `Half Bath`

- **Meaning:** Half Bathrooms (Above Grade)
- **Description:** Number of half bathrooms above grade.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 3
- **Example values:** 0, 1, 2

## `Bedroom AbvGr`

- **Meaning:** Bedrooms Above Grade
- **Description:** Number of bedrooms located above ground level.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 8
- **Example values:** 3, 2, 1, 4, 6

## `Kitchen AbvGr`

- **Meaning:** Kitchens Above Grade
- **Description:** Number of kitchens located above ground level.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 4
- **Example values:** 1, 2, 3, 0

## `Kitchen Qual`

- **Meaning:** Kitchen Quality
- **Description:** Quality of the kitchen (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 5
- **Example values:** TA, Gd, Ex, Fa, Po

## `TotRms AbvGrd`

- **Meaning:** Total Rooms Above Grade
- **Description:** Total number of rooms above grade, excluding bathrooms.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 14
- **Example values:** 7, 5, 6, 8, 4

## `Functional`

- **Meaning:** Home Functionality
- **Description:** Overall functionality of the home (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 8
- **Example values:** Typ, Mod, Min1, Min2, Maj1

## `Fireplaces`

- **Meaning:** Fireplaces
- **Description:** Number of fireplaces in the property.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 5
- **Example values:** 2, 0, 1, 3, 4

## `Fireplace Qu`

- **Meaning:** Fireplace Quality
- **Description:** Quality of the fireplace (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 1422 (48.532%)
- **Unique values:** 5
- **Example values:** Gd, TA, Po, Ex, Fa

## `Garage Type`

- **Meaning:** Garage Location
- **Description:** Location of the garage relative to the home.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 157 (5.358%)
- **Unique values:** 6
- **Example values:** Attchd, BuiltIn, Basment, Detchd, CarPort

## `Garage Yr Blt`

- **Meaning:** Garage Construction Year
- **Description:** Original year the garage was constructed.
- **Semantic group:** `temporal`
- **Pandas dtype:** `float64`
- **Missing values:** 159 (5.427%)
- **Unique values:** 103
- **Example values:** 1960.0, 1961.0, 1958.0, 1968.0, 1997.0

## `Garage Finish`

- **Meaning:** Garage Interior Finish
- **Description:** Interior finish of the garage (finished, unfinished, rough).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 159 (5.427%)
- **Unique values:** 3
- **Example values:** Fin, Unf, RFn

## `Garage Cars`

- **Meaning:** Garage Capacity
- **Description:** Number of cars the garage can accommodate.
- **Semantic group:** `numeric_discrete`
- **Pandas dtype:** `float64`
- **Missing values:** 1 (0.034%)
- **Unique values:** 6
- **Example values:** 2.0, 1.0, 3.0, 0.0, 4.0

## `Garage Area`

- **Meaning:** Garage Area
- **Description:** Square footage of the garage.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `float64`
- **Missing values:** 1 (0.034%)
- **Unique values:** 603
- **Example values:** 528.0, 730.0, 312.0, 522.0, 482.0

## `Garage Qual`

- **Meaning:** Garage Quality
- **Description:** Quality of the garage (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 159 (5.427%)
- **Unique values:** 5
- **Example values:** TA, Fa, Gd, Ex, Po

## `Garage Cond`

- **Meaning:** Garage Condition
- **Description:** Condition of the garage (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 159 (5.427%)
- **Unique values:** 5
- **Example values:** TA, Fa, Gd, Ex, Po

## `Paved Drive`

- **Meaning:** Paved Driveway
- **Description:** Whether the driveway is paved (Y/N/P).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 3
- **Example values:** P, Y, N

## `Wood Deck SF`

- **Meaning:** Wood Deck Area
- **Description:** Square footage of wood deck area.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 380
- **Example values:** 210, 140, 393, 0, 212

## `Open Porch SF`

- **Meaning:** Open Porch Area
- **Description:** Square footage of the open porch.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 252
- **Example values:** 62, 0, 36, 34, 82

## `Enclosed Porch`

- **Meaning:** Enclosed Porch Area
- **Description:** Square footage of enclosed porch area.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 183
- **Example values:** 0, 170, 184, 154, 80

## `3Ssn Porch`

- **Meaning:** Three-Season Porch Area
- **Description:** Square footage of three-season porch area.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 31
- **Example values:** 0, 238, 224, 144, 508

## `Screen Porch`

- **Meaning:** Screen Porch Area
- **Description:** Square footage of screened porch area.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 121
- **Example values:** 0, 120, 144, 140, 210

## `Pool Area`

- **Meaning:** Pool Area
- **Description:** Total pool area in square feet.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 14
- **Example values:** 0, 144, 480, 576, 555

## `Pool QC`

- **Meaning:** Pool Quality
- **Description:** Quality of the pool (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 2917 (99.556%)
- **Unique values:** 4
- **Example values:** Ex, Gd, TA, Fa

## `Fence`

- **Meaning:** Fence Quality
- **Description:** Quality of the fence (ordinal).
- **Semantic group:** `categorical_ordinal`
- **Pandas dtype:** `object`
- **Missing values:** 2358 (80.478%)
- **Unique values:** 4
- **Example values:** MnPrv, GdPrv, GdWo, MnWw

## `Misc Feature`

- **Meaning:** Miscellaneous Feature
- **Description:** Miscellaneous feature not covered in other categories.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 2824 (96.382%)
- **Unique values:** 5
- **Example values:** Gar2, Shed, Othr, Elev, TenC

## `Misc Val`

- **Meaning:** Miscellaneous Value
- **Description:** Value of the miscellaneous feature in USD.
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 38
- **Example values:** 0, 12500, 500, 700, 400

## `Mo Sold`

- **Meaning:** Month Sold
- **Description:** Month the property was sold.
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 12
- **Example values:** 5, 6, 4, 3, 1

## `Yr Sold`

- **Meaning:** Year Sold
- **Description:** Year the property was sold.
- **Semantic group:** `temporal`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 5
- **Example values:** 2010, 2009, 2008, 2007, 2006

## `Sale Type`

- **Meaning:** Sale Type
- **Description:** Type of sale (normal, auction, family, etc.).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 10
- **Example values:** WD , New, COD, ConLI, Con

## `Sale Condition`

- **Meaning:** Sale Condition
- **Description:** Condition of the sale (normal, partial, abnormal).
- **Semantic group:** `categorical_nominal`
- **Pandas dtype:** `object`
- **Missing values:** 0 (0.0%)
- **Unique values:** 6
- **Example values:** Normal, Partial, Family, Abnorml, Alloca

## `SalePrice`

- **Meaning:** Sale Price
- **Description:** Final sale price of the property in USD (this is the target variable).
- **Semantic group:** `numeric_continuous`
- **Pandas dtype:** `int64`
- **Missing values:** 0 (0.0%)
- **Unique values:** 1032
- **Example values:** 215000, 105000, 172000, 244000, 189900
