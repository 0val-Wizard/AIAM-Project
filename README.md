# AIAM-Project
AI for Advanced Manufacturing(AIAM) is a Year 3 Elective Module in TP. It introduces knowledge and skills needed to implement Artificial Intelligence (AI) in cybersecurity. Topics covered in the subject will include an introduction to cybersecurity, implementations of AI in cybersecurity, and defending against threats targeting AI technologies.

## What did I do for my AIAM Project? 
I worked on the following;
1) Pipeline
2) Report/Presentation

## What was the focus of my Pipeline?
- Predictive maintenance for industrial machinery using sensor telemetry
- Goal: detect early signs of malfunction or failure before they escalate

## Detailed Summary of my Pipeline:
1. Data Loading & Exploration
- Loaded dataset containing compressor sensor readings (oil level, motor current, pressure, etc.).
- Performed exploratory analysis:
  - Checked datatypes, missing values, duplicates.
  - Resampled time-series (hourly means).
  - Plotted distributions, scatter plots, time-series trends.
  - Investigated skewness, kurtosis, correlations.
  - Analyzed oil levels, motor current, pressure switches.
- Applied stationarity checks (ADF test, ACF/PACF plots, STL decomposition) → to see seasonality and trends.

2. Data Preprocessing
- Dropped redundant features: e.g., H1, Reservoirs, COMP, DV_eletric, MPG (high multicollinearity > 0.8).
- Cleaned timestamp → converted to datetime, sorted, reset index.
- Dealt with missing values.
- Scaling applied: MinMaxScaler, RobustScaler, Winsorization for outlier control.
- Created binary flags (e.g., oil_low_flag, motor_inactive).

3. Feature Engineering
- Derived temporal features: rolling mean, rolling std, lag features.
- Built difference features (rate of change).
- Added statistical features (variance, z-score, correlation-based combinations).
- Incorporated time-based aggregations.

4. Modeling Approaches
- While later parts of the notebook (not shown yet in the snippet) typically cover models, the preparation suggests:
  - Unsupervised anomaly detection methods:
    - Empirical Covariance
    - DBSCAN (density-based clustering for anomaly regions)
  - Likely supplemented with other outlier detection methods (Isolation Forest, One-Class SVM).


## Summary of Pipeline
- Raw compressor sensor data ingestion.
- Data cleaning & redundancy removal.
- Exploratory analysis of key variables (oil, motor current, pressure).
- Feature engineering: temporal, statistical, and categorical flags.
- Scaling & normalization.
- Anomaly detection modeling (unsupervised).
