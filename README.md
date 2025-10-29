# ✈️ Flight Delay Prediction (Arrival Delay > 15 Minutes)

This project predicts whether a flight will arrive **more than 15 minutes late** using flight schedule and operational data from the U.S. Department of Transportation.  
It demonstrates a full machine learning pipeline — from data exploration and feature engineering to model training and evaluation.

---

## 🧩 Project Overview

The goal is to build a classification model that predicts whether a flight will be **delayed (1)** or **on time (0)** before take-off.  
This prediction can help airlines and passengers plan better, reduce wait times, and optimize flight operations.

---

## 📂 Dataset

The dataset used is the **On-Time Reporting Carrier On-Time Performance (1987-present)** from the U.S. Bureau of Transportation Statistics.  
It contains flight-level information such as:

- **Date and time of flight**
- **Airline**
- **Origin and destination airports**
- **Distance**
- **Scheduled and actual departure/arrival times**
- **Delay indicators**

---

## ⚙️ Features Used for Prediction

Key features selected for the model include:

- `Quarter`, `Month`, `DayofMonth`, `DayOfWeek`
- `Reporting_Airline`, `Origin`, `Dest`
- `Distance`, `DepHourofDay`
- Target variable: `is_delay` (1 = Delayed > 15 min, 0 = On-time)

---

## 🧠 Machine Learning Model

The baseline model is a **Logistic Regression Classifier**, built using `scikit-learn`.

- Training data: 70%
- Validation data: 10%
- Testing data: 20%

### ⚖️ Evaluation Metrics
- **Accuracy**: ~79%
- **Precision**: 0.55  
- **Recall (Sensitivity)**: 0.00 (indicates imbalance)
- **Specificity**: 0.99  
- **AUC Score**: 0.50  

> The model performs well in detecting on-time flights but struggles with imbalanced classes — future improvements could involve resampling or using ensemble methods.

---

## 📊 Data Visualization Insights

Exploratory Data Analysis (EDA) showed:

- **Evening flights** have slightly higher chances of delay.  
- **Summer months** (June–August) tend to see more delays.  
- **Airlines and airports** differ significantly in their delay ratios.  
- **Flight distance** is not a major factor in short delays.

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/prenasanu/Flight-delay-ML.git
   cd Flight-delay-ML


2. **Install dependencies**
   ```bash
   pip install -r requirements.txt

3. **Run Jupyter Notebook
jupyter notebook onpremises.ipynb
4. **Expected Output

Data exploration plots for delays by time, month, airline, etc.

Trained logistic regression model with metrics and ROC plot.

##Author
Prerana Manandhar
u3280005
Masters of Datascience, University of Canberra
