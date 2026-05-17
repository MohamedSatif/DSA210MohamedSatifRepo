# Temperature and Nutrient Stability: The Effect of Heat on Calcium Content in Milk

> *Are we unknowingly losing calcium every time we heat our milk?*

**DSA 210 – Introduction to Data Science (Spring 2026)**  
**Student:** Mohamed Satif

---

## Research Question

Does heating milk affect its calcium content enough to impact its nutritional reliability?

---

## Motivation

Milk and plant-based alternatives are widely recognized as primary dietary sources of calcium — a mineral essential for bone strength, muscle function, and overall physical performance. As someone who regularly goes to the gym and has experienced multiple bone fractures, maintaining adequate calcium intake is personally important to me.

This led me to question whether common habits, such as heating milk, could influence its nutritional reliability. In a previous experiment, I investigated how temperature affects the calcium content of hazelnut milk, which provided a foundation for understanding temperature-related changes at a chemical level. This project builds on that by exploring whether such changes have practical implications for people who rely on milk as a consistent calcium source.

---

## Hypothesis

Increasing heating temperature and duration will reduce the measurable soluble or ionic calcium fraction in milk due to heat-induced mineral redistribution and calcium-phosphate precipitation. However, this reduction is expected to follow a diminishing nonlinear trend rather than a continuous linear decline, since milk contains a finite amount of calcium available for redistribution.

---

## Data Sources

| # | Study | Data Used |
|---|---|---|
| 1 | Mejares et al. (2023) | Ca²⁺ activity and pH at 0°C, 85°C, 95°C |
| 2 | Magee & Harvey (1926) | Soluble calcium loss after heating |
| 3 | Schreiber et al. (2022) | Calcium-phosphate precipitation thresholds |
| 4 | Pouliot et al. (1999) | Relative calcium retention (%) |
| 5 | Rahimi et al. (2024) | Calcium retention under UHT treatment |
| 6 | On-Nom et al. (2010) | Ionic Ca²⁺ activity from 20°C–110°C |
| 7 | Tessier & Rose (1958) | Early ionic calcium measurements |
| 8 | Choi et al. (2013) | Soluble calcium in commercial milk |

### Data Collection Process

Data was collected through a systematic literature review. Studies were selected based on:
- heating temperature
- heating duration
- milk type
- calcium-related outcome measured

The final dataset combines experimental measurements from multiple peer-reviewed dairy science studies published between 1926 and 2024.

---

## Dataset Overview

The compiled dataset contains:
- Temperature measurements ranging from 0°C to 135°C
- Multiple milk categories (bovine, buffalo, skim, semi-skim, mixed blends)
- Several heating treatments (pasteurization, HTST, UHT, calcium-sequestering salts)
- Multiple calcium-related indicators:
  - ionic calcium activity (mM)
  - soluble calcium concentration
  - calcium retention (%)
  - pH measurements

### Dataset Variables

| Variable | Description |
|---|---|
| source | Research study source |
| year | Publication year |
| milk_type | Milk category/type |
| treatment | Heat treatment or additive condition |
| temperature_C | Heating temperature in Celsius |
| calcium_activity_mM | Measured ionic calcium or calcium retention value |
| pH | Milk acidity value |

---

## Methods Overview

### Exploratory Data Analysis (EDA)

EDA was conducted to visualize:
- calcium activity changes across temperature ranges
- pH variation under heating
- differences between milk types
- trends across historical studies

Visualizations include:
- scatter plots
- regression curves
- heat-treatment comparison plots
- clustering visualizations

---

## Machine Learning Analysis

The project applies supervised and unsupervised machine learning techniques to model heat-induced calcium changes.

### 1. Regression Analysis

**Goal:** Predict ionic calcium activity from temperature.

Models used:
- Linear Regression
- Polynomial Regression (degree = 2)

Evaluation methods:
- R² score
- Leave-One-Out Cross Validation (LOO-CV)

The polynomial model was specifically chosen to test the hypothesis that calcium reduction follows a nonlinear diminishing trend rather than a perfectly linear decline.

---

### 2. Classification Analysis

**Goal:** Predict heat treatment severity from calcium activity and pH values.

Heat severity classes:
- Low Heat: 0–60°C
- Medium Heat: 61–90°C
- High Heat: >90°C

Models used:
- Decision Tree Classifier
- Random Forest Classifier

Evaluation methods:
- 5-Fold Cross Validation
- Classification reports
- Confusion matrices
- Feature importance analysis

---

### 3. Clustering Analysis

**Goal:** Determine whether milk samples naturally group according to heating intensity without predefined labels.

Method used:
- K-Means Clustering

---

## Key Findings

### Regression Results

- Both regression models identified a strong negative relationship between temperature and ionic calcium activity.
- Polynomial regression outperformed simple linear regression, supporting the hypothesis that calcium decline follows a nonlinear diminishing pattern.
- Ionic calcium activity decreases rapidly at moderate temperatures before stabilizing at higher temperatures.

---

### Classification Results

- Decision Tree and Random Forest models successfully classified milk samples into low, medium, and high heat categories using calcium activity and pH values.
- Random Forest achieved the highest classification accuracy.
- Feature importance analysis showed that temperature and calcium activity were the strongest predictors of heating severity.

---

### Clustering Results

- K-Means clustering naturally separated samples into low-, medium-, and high-heat groups.
- The clustering structure aligned closely with known thermal processing categories.
- Silhouette analysis confirmed meaningful cluster separation.

---

## Main Conclusion

Heating milk measurably reduces ionic and soluble calcium availability, particularly at moderate-to-high processing temperatures. Machine learning analyses demonstrated that these changes are systematic, predictable, and strongly associated with thermal treatment intensity.

The results support the hypothesis that calcium reduction follows a nonlinear diminishing trend rather than a continuous linear decline.

Although total calcium may not completely disappear, heat-induced redistribution and precipitation significantly affect the measurable ionic calcium fraction, which may influence nutritional reliability.

---

## Limitations

- Data is sourced from published literature rather than original laboratory experiments
- Experimental methods vary substantially across studies
- Milk types differ between studies (bovine, buffalo, skim, semi-skim), limiting direct comparability
- Some studies report ionic calcium while others report soluble calcium or retention percentages
- Sample size remains relatively small for machine learning applications
- Bioavailability of calcium after heating is not directly measured in most studies

---

## Future Improvements

Potential extensions of this project include:
- conducting original laboratory experiments for standardized measurements
- separating ionic calcium and retention-percentage datasets into independent models
- testing additional regression methods such as exponential decay models
- investigating calcium bioavailability after digestion
- comparing dairy milk with plant-based alternatives under identical thermal conditions

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

## AI Tools Disclosure

In accordance with DSA 210 academic integrity guidelines, AI assistance was used in this project. Claude (Anthropic) was used to help structure the README, review writing, and suggest analysis approaches.
