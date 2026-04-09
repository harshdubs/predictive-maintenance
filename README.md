# 🔧 Predictive Maintenance & Anomaly Detection

A machine learning project that detects early warning signs of equipment failure in industrial sensor data — before the machine actually breaks down.

---

## 📌 The Problem

In manufacturing, unplanned machine breakdowns are extremely costly — they stop entire production lines, waste materials, and delay delivery. Most plants run on **reactive maintenance** (fix it after it breaks) or **scheduled maintenance** (fix it on a calendar, regardless of actual condition).

This project builds a smarter approach: **predictive maintenance** — flag anomalous sensor behaviour *before* failure occurs.

---

## 🧠 Approach

1. **Data:** 6 months of multi-sensor time-series data from industrial machines (temperature, vibration, pressure, current)
2. **Cleaning:** Python pipeline to handle missing readings, sensor dropouts, and timestamp gaps
3. **Model:** Isolation Forest — an unsupervised anomaly detection algorithm well-suited for sensor data with no labelled failures
4. **Output:** Anomaly score per reading + automated flagging of high-risk time windows
5. **Reporting:** SQL-backed priority report showing which machines need attention and when

---

## 📈 Results

- **87% precision** on flagged pre-failure windows (validated against known breakdown events)
- Detected anomalous patterns **avg. 18 hours before** actual failure
- Automated reporting replaced manual daily sensor review

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python (Pandas, NumPy) | Data cleaning & feature engineering |
| Scikit-learn | Isolation Forest model |
| Matplotlib, Seaborn | Sensor visualisation & anomaly plots |
| SQL | Anomaly flag reporting & prioritisation |

---

## 📁 Project Structure

```
predictive-maintenance/
│
├── data/
│   └── sensor_data_sample.csv
│
├── notebooks/
│   └── 01_data_exploration.ipynb
│   └── 02_feature_engineering.ipynb
│   └── 03_anomaly_detection_model.ipynb
│   └── 04_results_and_reporting.ipynb
│
├── sql/
│   └── anomaly_priority_report.sql
│
└── README.md
```

---

## 🚀 How to run

```bash
git clone https://github.com/cosmicskull711/predictive-maintenance
cd predictive-maintenance
pip install -r requirements.txt
jupyter notebook notebooks/01_data_exploration.ipynb
```

---

## 👤 Author

**Harsh Dubey** — [LinkedIn](https://www.linkedin.com/in/harsh-dubey-1b169a242) · [GitHub](https://github.com/harshdubs)
