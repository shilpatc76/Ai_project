Employee Email Sentiment Analysis & Engagement Insights

This project analyzes employee communication patterns using Natural Language Processing (NLP) and Machine Learning techniques. The goal is to evaluate employee sentiment, detect engagement trends, identify high-risk employees, and build a predictive model based on communication behavior.

The dataset used for this project is test.csv, containing unlabeled internal messages.

📁 Project Contents
File/Folder	Description
employee_sentiment.ipynb	Main notebook with full implementation
predictions.csv	Dataset with sentiment labels added
visualizations/	Folder containing generated graphs and plots
model.pkl	Trained sentiment regression model
README.md	Project documentation (this file)
requirements.txt	List of libraries used
🎯 Project Objectives

This project fulfills the following key goals:

Automatically classify sentiment for employee messages

Perform full exploratory data analysis (EDA)

Compute monthly sentiment scores per employee

Rank employees based on communication tone

Detect flight-risk behavior patterns

Develop a predictive model based on engagement metrics

🧩 Task Breakdown
1️⃣ Sentiment Labeling

Text preprocessing performed on email content

Each message labeled as:

Positive

Neutral

Negative

A new feature Sentiment was added to the dataset.

2️⃣ Exploratory Data Analysis (EDA)

Analysis includes:

✔ Missing value detection
✔ Text length distribution
✔ Sentiment distribution visualization
✔ Time-based message trends

Generated visualizations stored in /visualizations.

3️⃣ Monthly Sentiment Scoring

Scoring logic:

Sentiment	Score
Positive	+1
Neutral	0
Negative	−1

Scores were aggregated monthly per employee and stored in the column:

➡ Monthly_Sentiment_Score

4️⃣ Employee Ranking

Two leaderboards were generated monthly:

🏆 Top 3 Positive employees

⚠️ Top 3 Negative employees

Sorting priority:

Score value

Alphabetical order (tie-breaking)

5️⃣ Flight-Risk Detection

A flight-risk employee is defined as:

An employee who sends 4 or more negative messages within any rolling 30-day window.

Output column added:

➡ Flight_Risk = Yes / No

6️⃣ Predictive Modeling

A supervised regression model was implemented using:

Message length

Word count

Average sentiment trend

Monthly message frequency

The goal was to predict sentiment score patterns.

The model was evaluated using:

Mean Squared Error (MSE)

R² Score

The final model is stored as model.pkl.

🧪 Tools & Technologies
Category	Tools
Language	Python
Machine Learning	Scikit-Learn (or PyTorch if used)
NLP	TF-IDF / Text Preprocessing
Visualization	Matplotlib, Seaborn
Storage	Pickle, CSV
📊 Key Insights Summary

(Replace with your actual results)

Total messages analyzed: —

Sentiment distribution: —

Top positive contributors: —

Top negative contributors: —

Identified flight-risk employees: —

Regression model performance (R²): —

▶️ Running the Project

Install dependencies:

pip install -r requirements.txt


Run notebook:

jupyter notebook employee_sentiment.ipynb
