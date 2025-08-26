# Aviation Crash Predictive Model

## Description
This project analyzes historical aviation crash data (1908–present) and predicts **high-fatality crashes** (≥10 fatalities). The model uses machine learning to identify factors contributing to severe crashes and provides insights into aviation safety.

## Dataset
- **File:** Airplane_Crashes_and_Fatalities_Since_1908.csv  
- **Source:** [Kaggle](https://www.kaggle.com/datasets/thedevastator/airplane-crashes-and-fatalities/data)  
- **Records:** 5,268 crashes  
- **Features:** Date, Time, Location, Operator, Aboard, Fatalities, Type, Registration, Country, etc.

## Steps
1. **Data Cleaning**
   - Dropped columns with >50% missing values
   - Filled missing numeric values with median
   - Filled missing categorical values with 'Unknown'
   - Converted Date/Time to datetime format
   - Extracted 'Country' from Location
   - Dropped low-variance columns

2. **Data Exploration (EDA)**
   - Distribution of Fatalities, People Aboard, and Fatality Rate
   - Scatterplot: Aboard vs Fatalities
   - Trend of crashes over years
   - Top 10 operators with most crashes

3. **Feature Engineering & Preprocessing**
   - Extracted Hour, Month, DayOfWeek from Date/Time
   - Target variable: `HighFatality` (1 if Fatalities ≥ 10 else 0)
   - Preprocessed numeric features (StandardScaler) and categorical features (OneHotEncoder)
   - Train/Test split (80/20)

4. **Model Training**
   - Logistic Regression (baseline)
   - Random Forest Classifier (main model)

5. **Model Evaluation**
   - Confusion Matrix
   - Classification Report (precision, recall, F1-score, accuracy)
   - Feature Importance

## Results
- **Model Accuracy:** ~76% (Random Forest / Logistic Regression)  
- **Key features impacting high-fatality crashes:** Aboard, Operator, Type, Hour

## How to Run
1. Clone the repository:
```bash
git clone https://github.com/yourusername/aviation-crash-prediction.git

Install required packages:
bash
pip install -r requirements.txt

Open and run the notebook in Jupyter or Google Colab:
bash
notebooks/aviation_project.ipynb

Step through the cells to reproduce data cleaning, EDA, modeling, and evaluation.
Author
Lex Yonjan Lama
