# 🏨 Hotel Booking Cancellation Prediction

### An End-to-End Data Science Project

This project was developed as part of the **YuvaIntern Junior Data Scientist Virtual Internship**. It demonstrates a complete data science workflow, from data cleaning and exploratory analysis through statistical modeling, machine learning, visualization, and business insights.

The project uses the **Hotel Booking Demand dataset** to investigate customer booking behavior and develop a machine learning model capable of predicting whether a hotel reservation will be cancelled.

---

## 📌 Project Overview

Hotel booking cancellations can cause significant challenges for hotels, including:

- Revenue loss
- Unoccupied rooms
- Inefficient resource allocation
- Demand-forecasting difficulties
- Operational uncertainty

**Data science lifecycle followed:**

```
Data Collection
      ↓
Data Cleaning & Preprocessing
      ↓
Exploratory Data Analysis
      ↓
Statistical Modeling
      ↓
Machine Learning
      ↓
Model Evaluation
      ↓
Data Visualization
      ↓
Business Insights
      ↓
Recommendations
```

---

## 🎯 Objectives

- Clean and preprocess the hotel booking dataset
- Handle missing values and duplicate records
- Detect and treat invalid records and outliers
- Perform exploratory data analysis
- Identify important patterns and relationships
- Formulate and test statistical hypotheses
- Develop a Logistic Regression model
- Develop and optimize a Random Forest classification model
- Perform cross-validation and hyperparameter tuning
- Evaluate model performance using appropriate metrics
- Identify important predictive features
- Communicate findings using effective visualizations
- Provide actionable business recommendations

---

## 📊 Dataset

**Dataset Name:** Hotel Booking Demand Dataset

The dataset contains reservation information for City Hotels and Resort Hotels, including booking dates, arrival information, lead time, guests, stay duration, room types, meal preferences, market segments, customer types, booking changes, previous cancellations, ADR, and cancellation status.

**Target Variable:** `is_cancelled`

| Value | Meaning |
|-------|---------|
| 0 | Booking was not cancelled |
| 1 | Booking was cancelled |

The cleaned dataset used during the project contains **87,203 records** and **36 columns**.

---

## 🗂️ Project Structure

```
Hotel_Booking_Cancellation_Project/
│
├── Data/
│   ├── hotel_bookings.csv
│   └── hotel_bookings_cleaned.csv
│
├── Notebooks/
│   ├── Week1_DataCleaning.ipynb
│   ├── Week2_EDA.ipynb
│   ├── Week3_Statistical_Modeling.ipynb
│   ├── Week4_Machine_Learning.ipynb
│   └── Week5_Data_Visualization.ipynb
│
├── Reports/
│   ├── Week1_Report.pdf
│   ├── Week2_EDA_Report.pdf
│   ├── Week3_Statistical_Modeling_Report.pdf
│   ├── Week4_Machine_Learning_Report.pdf
│   ├── Week5_Visualization_Report.pdf
│   └── Final_Project_Report.pdf
│
├── Visualizations/
│   ├── Figure1_Hotel_Type.png
│   ├── Figure2_Hotel_Pie.png
│   ├── Figure3_Cancellation.png
│   ├── Figure4_CustomerType.png
│   ├── Figure5_MarketSegment.png
│   ├── Figure6_MealPreference.png
│   ├── Figure7_TopCountries.png
│   ├── Figure8_ADRDistribution.png
│   ├── Figure9_LeadTime.png
│   ├── Figure10_ADR_Boxplot.png
│   ├── Figure11_Guests_vs_ADR.png
│   ├── Figure12_TotalNights.png
│   ├── Figure13_Heatmap.png
│   ├── Figure14_FeatureImportance.png
│   └── Figure15_ROC.png
│
├── Models/
│   └── random_forest_model.pkl
│
└── README.md
```

---

## 📅 Weekly Project Breakdown

### Week 1 — Data Gathering, Cleaning & Preprocessing

The first stage prepared the raw dataset for analysis.

**Major tasks:**
- Loaded and inspected the dataset using Pandas
- Identified and handled missing values
- Removed columns with excessive missing values
- Removed duplicate records
- Removed invalid bookings containing zero guests
- Identified and treated outliers
- Converted appropriate variables to categorical data types
- Created an arrival date feature
- Performed feature engineering

**Engineered Features:**
- `total_guests`
- `total_nights`
- `is_family`
- `booking_status`

**Output:** `hotel_bookings_cleaned.csv`

---

### 📈 Week 2 — Exploratory Data Analysis

The second stage focused on understanding the cleaned dataset through statistical summaries and visualization.

**Techniques Used:**
- Descriptive statistics (mean, median, mode, standard deviation, variance)
- Histograms
- Box plots
- Bar charts
- Pie charts
- Scatter plots
- Correlation analysis
- Heatmaps
- Hypothesis testing

---

### 📐 Week 3 — Statistical Modeling & Hypothesis Testing

The third stage focused on statistical modeling.

**Research Question:**
Can booking characteristics such as lead time, ADR, number of guests, and booking changes predict whether a hotel booking will be cancelled?

**Hypotheses:**
- **H₀:** Booking characteristics do not significantly affect hotel booking cancellations.
- **H₁:** At least one booking characteristic significantly affects hotel booking cancellations.

**Model:** Logistic Regression

**Predictor Variables:**
- `lead_time`
- `adr`
- `total_guests`
- `total_nights`
- `previous_cancellations`
- `booking_changes`
- `days_in_waiting_list`

The model was evaluated using coefficients, standard errors, z-statistics, p-values, confidence intervals, and Pseudo R².

---

### 🤖 Week 4 — Machine Learning Model Development

The fourth stage developed a machine learning classification model.

**Algorithm:** Random Forest Classifier

Random Forest was selected because it:
- Handles nonlinear relationships
- Combines multiple decision trees
- Reduces overfitting
- Performs well on classification problems
- Provides feature importance
- Is relatively robust to noisy data

**Model Optimization:**
Cross-validation was used during model development, and GridSearchCV was used for hyperparameter tuning.

Parameters considered included:
- `n_estimators`
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`

The optimized model was evaluated on an unseen test dataset.

**📊 Model Evaluation**

The Random Forest model was evaluated using:
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix
- ROC Curve
- ROC-AUC

These metrics provide a comprehensive view of the model's classification performance.

---

### 📊 Week 5 — Data Visualization & Communication

The fifth stage transformed analytical results into an effective visual story.

**Visualizations Created:**
- Hotel Type Distribution
- Hotel Type Percentage
- Booking Cancellation Status
- Customer Type Distribution
- Market Segment Distribution
- Meal Preference Distribution
- Top 10 Countries
- ADR Distribution
- Lead Time Distribution
- ADR by Hotel Type
- Total Guests vs ADR
- Total Nights Distribution
- Correlation Heatmap
- Random Forest Feature Importance
- ROC Curve

Each visualization was designed with clear titles, labels, appropriate chart types, interpretation, and business relevance.

---

## 🔍 Key Insights

- City Hotels account for a larger proportion of reservations compared with Resort Hotels.
- The majority of customers belong to the Transient customer category.
- Online Travel Agencies represent a major source of reservations.
- Booking characteristics such as lead time and previous cancellation history provide useful information for predicting cancellation behavior.
- Average Daily Rate varies across hotel types, customer categories, and market segments.
- `booking_changes` represents the number of modifications made to a reservation before arrival and provides behavioral information about booking uncertainty.
- Random Forest provides a nonlinear machine learning approach for identifying patterns associated with booking cancellations.

---

## 💡 Business Recommendations

1. **Monitor High-Risk Bookings** — Bookings with characteristics associated with higher cancellation probability can be monitored more closely.
2. **Analyze Previous Cancellation History** — Customers with previous cancellations may require additional confirmation or targeted communication.
3. **Optimize Reservation Policies** — Cancellation policies can be designed based on observed customer behavior.
4. **Improve Demand Planning** — Cancellation predictions can help hotels estimate actual occupancy more accurately.
5. **Optimize Pricing** — ADR and booking behavior can be analyzed together to improve pricing and revenue-management strategies.
6. **Strengthen Customer Retention** — Hotels can proactively communicate with customers whose bookings show a higher cancellation risk.

---

## ⚠️ Limitations

- The analysis is based on historical booking data.
- External factors such as weather, economic conditions, holidays, and unexpected events are not included.
- The selected machine learning features represent only a subset of the available information.
- Model performance depends on the quality and representativeness of historical data.
- Logistic Regression assumes a specific relationship between predictors and the log-odds of the outcome.
- Random Forest is less interpretable than a simple statistical model.

---

## 🚀 Future Scope

- Comparing Random Forest with XGBoost and other ensemble algorithms
- Performing more extensive feature engineering
- Including seasonal and holiday information
- Incorporating real-time booking information
- Developing a web application for cancellation prediction
- Deploying the model as an API
- Creating an interactive dashboard using Power BI, Tableau, or Plotly
- Implementing automated model monitoring
- Retraining the model periodically using new booking data

---

## 🛠️ Technologies Used

`Python` · `Pandas` · `NumPy` · `Matplotlib` · `Seaborn` · `Scikit-learn` · `Statsmodels` · `Jupyter Notebook`

---

## 📦 Installation

Clone the repository:
```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
```

Navigate to the project directory:
```bash
cd Hotel_Booking_Cancellation_Project
```

Install the required packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels jupyter
```

Launch Jupyter Notebook:
```bash
jupyter notebook
```

---

## ▶️ How to Run

1. Place the dataset inside the `Data/` directory.
2. Run the notebooks in order:

```
Week 1 → Week 2 → Week 3 → Week 4 → Week 5
```

3. Review generated visualizations and model results.
4. Refer to the final project report for the complete analysis.

---

## 📁 Deliverables

- Raw dataset
- Cleaned dataset
- Week 1–5 notebooks
- Visualization outputs
- Statistical modeling results
- Machine learning model
- Weekly reports
- Final project report
- README documentation

---

## 👨‍💻 Author

**Abhiram Chander Sai Jandhyala**
B.Tech – Information Technology
J.B. Institute of Engineering & Technology
YuvaIntern – Junior Data Scientist Intern

---

## 📜 Internship

This project was completed as part of the **YuvaIntern Junior Data Scientist Virtual Internship**.

The project demonstrates practical experience in:

`Data Preprocessing` + `Exploratory Data Analysis` + `Statistical Analysis` + `Machine Learning` + `Data Visualization` + `Business Communication`

---

## ⭐ Project Outcome

The project demonstrates how raw hotel reservation data can be transformed into actionable business insights through a complete data science workflow. By combining statistical analysis, machine learning, and visual storytelling, the project provides a structured approach to understanding and predicting hotel booking cancellations.

---

## 📌 Note

Update the exact model performance metrics in this README using the actual results produced by the final notebook. Avoid using estimated accuracy, precision, recall, F1-score, or ROC-AUC values.
