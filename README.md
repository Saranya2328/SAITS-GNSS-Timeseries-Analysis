# SAITS-Based GNSS Time Series Modeling and Event Analysis #

## Project Overview ##

This project focuses on the preprocessing, modeling, and analysis of GNSS satellite time-series data using a deep learning–based SAITS model. The work involves filtering GPS-only constellation data, temporal aggregation from seconds to hourly resolution, training a SAITS deep learning model, visualizing temporal variations, and evaluating model performance using standard metrics.

This work was carried out as part of my role as a Lab Engineer at IIT Tirupati Navavishkar I-Hub Foundation, under research and development activities related to GNSS data analysis.

## Problem Statement ##

Raw GNSS data contains multi-constellation satellite measurements at high temporal resolution (seconds-level), making it noisy and computationally expensive for modeling. Additionally, accurate modeling of GPS-only signals is essential for reliable temporal analysis and event-based studies.

## Objectives ##

- Filter multi-constellation GNSS data to retain GPS-only signals
- Convert seconds-level timestamps into hourly time-series data
- Train a SAITS deep learning model on processed GNSS data
- Visualize temporal trends and event-based anomalies
- Evaluate model performance using quantitative metrics

## Dataset Description ##

*Input Data*:  Raw GNSS satellite data

*Constellations*:  Multiple (filtered to GPS only)

*Temporal Resolution*:  Seconds → Minutes → Hourly

*Data Type*:  Time-series measurements with multiple satellite-related parameters

## Methodology (Pipeline) ##

**1. Combined Preprocessing**

 *Combined_code.ipynb*
- Filtered out non-GPS constellations
  
- Retained only GPS satellite observations
  
- Converted timestamps:
  
        Seconds → Minutes
        Minutes → Hourly aggregation
  
- Generated clean and uniform GPS time-series data for modeling
  
- This combined preprocessing pipeline improves efficiency, reproducibility, and clarity.

**2. SAITS Deep Learning Model**

*Traning_Model.ipynb*
- Implemented and trained SAITS (Self-Attention-based Imputation for Time Series)
- SAITS is a deep learning model designed for time-series learning using attention mechanisms
- Applied to hourly GPS GNSS data for prediction / imputation tasks

**3. Visualization & Event Analysis**

*Plotting_Phase.ipynb*
- Phase-wise visualization of GNSS time-series behavior

*Plotting_EventDays.ipynb*
- Highlighted and analyzed specific event days

*Plotting_EventMonths.ipynb*
- Month-wise visualization of event patterns
- Line graphs used to observe:
     Temporal trends
     Anomalies
     Event-driven variations

**4. Model Evaluation**

*Calculated_Metrics.ipynb*
- Computed quantitative performance metrics
- Used to assess the accuracy and reliability of the SAITS model output

## Technologies & Libraries Used ##
**Programming Language**
- Python
  
**Data Processing & Analysis**
- numpy
- pandas
  
**Visualization**
- matplotlib
- seaborn
  
**Deep Learning & Modeling**
- PyTorch / SAITS framework (as used in implementation)
- Attention-based neural network architecture

**Time-Series Handling**
- Pandas datetime utilities
- Time-based resampling and aggregation

**Evaluation Metrics**
- Standard regression / error metrics (used in Calculated_Metrics.ipynb)

## Evaluation Metrics ##

The model performance was evaluated using appropriate statistical metrics to quantify prediction/imputation accuracy and temporal consistency. These metrics help validate the effectiveness of the SAITS model on GNSS time-series data.

## Results & Observations ##

- GPS-only preprocessing significantly improved data consistency
- Hourly aggregation reduced noise while preserving temporal trends
- SAITS effectively captured temporal dependencies in GNSS signals
- Event-day and event-month visualizations revealed meaningful variations
