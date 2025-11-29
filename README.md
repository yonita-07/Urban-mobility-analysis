# Urban Mobility Delay Analysis
 A Complete end-to-end data science project with EDA, feature engineering and predictive modeling.
 ## Overview:
 This project analyzes 77k train records from 20 major German cities and builds a model to classify whether a train will be delayed.
 It includes:
 - Data cleaning
 - Exploratory Data analysis (EDA)
 - Visualisations
 - Feature engineering
 - Model training using Logistic Regression
 - Hyperparameter tuning
 - Evaluation
 - Final Insights

## Project Structure

# Project tree

Urban_Mobility_Analysis/
 * [data](Urban_Mobility_Analysis/data)
   * [cleaned_train_delays_full.csv](Urban_Mobility_Analysis/data/cleaned_train_delays_full.csv)
 * [notebooks](Urban_Mobility_Analysis/notebooks)
   * [urban-mobility-analysis-code.ipynb](Urban_Mobility_Analysis/notebooks/urban-mobility-analysis-code.ipynb)
   * [report](Urban_Mobility_Analysis/notebooks/report)
     * [urban_mobility_analysis.ipynb](Urban_Mobility_Analysis/notebooks/report/urban_mobility_analysis.ipynb)
 * [README.md](Urban_Mobility_Analysis/README.md)

## Data Description
- **Dates covered:** July-September 2024
- **Staions:** 20 largest cty main stations (HBF) in Germany
- **Columns include:**
    - date
    - Hbf(staiton)
    - scheduled_time
    - expected_time
    - train_model
    - route
    - platform
    - real_time_due_to_delay
    - has_delay(target_variable)

## Key insights from Analysis
**1.On-time vs Delayed Trains**
   - ~22% of all trians experienced delays.
    
**2.Delay Patterns**
   - Delay peaks during morning and evening rush hours.
   - Some stations consistently show higher delay frequencies.
    
**3.Daily trend**
  - Delay rates fluctuates based on operational load and weekday patterns.
    
**4.Feature relationships**
 - Station,route and train model influence delay probability.

## Machine Learning Model
**Model used:** Logistic Regression

**Hyperparameter tuning:** RandomizedSearchCV

**Final Model Performance**

|**Metric**    |**Score**|
|--------------|---------|
|Accuracy      | 84.89%  |
|Precision     | 83.82%  |
|Recall        | 81.75%  |
|F1 Score      | 82.77%  |

The model performs well despite natural class imbalance.

## Visualizations included
- Delay distribution histogram
- Delay by station
- Delay patterns by hour of the day
- Delay trend over time
All charts included in the project report notebook- urban_mobility_analysis.ipynb

## Conclusion
- Train delays show clear hourly and station-based patterns.
- A simple Logistic Regression model is able to predict delays with 85% accuracy.
- Operational factors(station, load, train type) play a major role in delay likelihood.

## Technologies Used
- Python 3.10+
- pandas, numpy, matplotlib, seaborn
- scikit-learn
- Jupyter Notebook
- Github for version control
  
## Future Work
- Integrate external factors (weather, events, maintenance logs)
- Experiment with gradient boosting models(XGBoost, LightGBM)
- Build an interactive Streamlit dashboard
- Add geospatial visualisation for route-level delay mapping
