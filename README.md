# Aviation Crash Predictive Model

## Description
This project analyzes historical aviation crash data (1908–present) and predicts high-fatality crashes (≥10 fatalities). It uses machine learning to identify key factors contributing to severe crashes.

## Dataset
- **File:** Airplane_Crashes_and_Fatalities_Since_1908.csv
- **Source:** [Kaggle](https://www.kaggle.com/datasets/thedevastator/airplane-crashes-and-fatalities/data)
- **Records:** 5,268 crashes
- **Features:** Date, Time, Location, Operator, Aboard, Fatalities, Type, Registration, Country, etc.

## Steps
1. **Data Cleaning**
   - Dropped columns with >50% missing
   - Filled missing numeric values with median
   - Filled missing categorical values with 'Unknown'
   - Converted Date/Time to datetime and standard format
   - Created 'Country' column from Location
   - Dropped low-variance columns

2. **Data Exploration (EDA)**
   - Distribution of Fatalities, People Aboard, Fatality Rate
   - Scatterplot of Aboard vs Fatalities
   - Crashes trend over years
   - Top 10 operators with most crashes

3. **Feature Engineering & Preprocessing**
   - Extracted Hour, Month, DayOfWeek
   - Target variable: HighFatality (1 if Fatalities ≥ 10)
   - Preprocessed numeric (StandardScaler) and categorical (OneHotEncoder)
   - Train/Test split (80/20)

4. **Model Training**
   - Logistic Regression (baseline)
   - Random Forest Classifier (main model)

5. **Model Evaluation**
   - Confusion Matrix
   - Classification Report: precision, recall, F1-score, accuracy
   - Feature Importance

## Results
- Model Accuracy: ~76%
- Key features affecting high-fatality crashes: Aboard, Operator, Type, Hour

## How to Run
1. Clone the repo:
```bash
git clone https://github.com/yourusername/aviation-crash-prediction.git
