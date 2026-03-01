🚆 Journey Time Prediction System (Linear Regression)
📌 Overview

This project builds a Journey Time Prediction System using Linear Regression on train operational data.
The goal is to predict total journey duration based on route distance and number of stops.

📊 Dataset Description

The raw dataset contains station-level records for multiple trains, including:

Train Number

Station Name

Arrival & Departure Time

Distance (cumulative)

Route Number

The dataset was transformed into a train-level modeling dataset (1 row per train).

🔧 Data Processing & Feature Engineering

Key steps performed:

Cleaned null and inconsistent time formats

Converted time into numeric duration (minutes)

Engineered features:

Total_Distance (max cumulative distance per train)

Number_of_Stops (count of stations per train)

Target variable:

Duration_Minutes

Final modeling dataset structure:

Train_No | Total_Distance | Number_of_Stops | Duration_Minutes

🤖 Model Development

Model Used: Linear Regression

Train-Test Split: 80% training / 20% testing

Evaluation Metrics:

RMSE: 235.20 minutes

MAE: 160.83 minutes

Model equation form:

Duration = b0 + b1*(Distance) + b2*(Number_of_Stops)

📈 Visual Analysis

The project includes:

Scatter Plot: Distance vs Journey Duration

Actual vs Predicted Journey Duration visualization

Correlation analysis between distance and duration

Observations:

Strong positive relationship between total distance and journey duration.

Significant variation for similar distances due to stop frequency and operational differences.

🧠 Key Insights

Distance alone does not fully explain journey time.

Number of stops significantly impacts total duration.

Operational variability leads to prediction error (reflected in RMSE).

🛠 Tech Stack

Python

Pandas

NumPy

Matplotlib

Scikit-learn

🚀 Future Improvements

Add more features (average speed, train type, route category)

Try Polynomial Regression or advanced ML models

Perform cross-validation for better generalization
