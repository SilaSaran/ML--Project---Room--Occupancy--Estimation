# ML_Project:

# 🏠 Room Occupancy Estimation Using Environmental Sensors

## 📌 Project Overview

This project aims to estimate the **number of occupants (0 to 3)** in a room using **non-intrusive environmental sensors**. 
It leverages machine learning to classify occupancy based on sensor readings such as temperature, light, sound, CO₂, and motion.

The goal is to develop a privacy-preserving and cost-effective solution for smart buildings, energy management, and space utilization.

---

## 📊 Dataset Description
- **Source**: Sensor data collected over 4 days in a 6m × 4.6m room
- **Instances**: 10,129
- **Features**: 18 (including timestamp, sensor readings, and occupancy labels)
- **Sensors Used**:
  - Temperature
  - Light
  - Sound
  - CO₂
  - PIR (Motion)
- **Ground Truth**: Manual recording of number of people present

---

## 🧪 Preprocessing Steps
- Handled missing values and duplicates
- Combined `Date` and `Time` into a unified `Date_time` column
- Created `Time_of_Day` feature (Morning, Afternoon, Evening, Night)
- Label encoded categorical features
- Removed highly correlated and redundant columns
- Treated outliers using IQR method

---

## 📈 Exploratory Data Analysis
- Count plots and pie charts for class distribution
- Boxplots and histograms for sensor behavior
- Correlation heatmap to identify feature relationships
- Scatterplots to visualize clustering patterns

---

## 🤖 Models Used
- Logistic Regression
- Decision Tree
- K-Nearest Neighbors (KNN)
- Gradient Boosting (best performer)

### 🛠️ Hyperparameter Tuning
Used `GridSearchCV` to optimize Gradient Boosting parameters:
- `n_estimators`
- `learning_rate`
- `max_depth`

---

## 📏 Evaluation Metrics
- **F1 Score** and **Accuaracy Score**
- Confusion Matrix
- Classification Report
- Feature Importance Analysis

---

🧠 Key Insights

Gradient Boosting outperformed other models with highest accuracy and F1 score.

Light and Sound sensors showed strong correlation with occupancy levels.

Time of Day significantly influenced occupancy patterns, with afternoons showing higher average counts.

No duplicate entries and minimal missing data ensured high data quality.

Outlier treatment improved model stability and performance.

## 🚀 Future Work
- Deploy model in real-time using edge devices or IoT platforms
- Expand to larger rooms or multi-room setups
- Integrate with smart building systems for automation
- Explore deep learning and ensemble methods for improved accuracy

---


## 🧪 Requirements
- Python 3.8+
- pandas, numpy, matplotlib, seaborn
- scikit-learn
  
