# Product-Led-Growth-PLG-analytics-pipeline
This project demonstrates a **Product-Led Growth (PLG) analytics pipeline** built with an open-source Kaggle dataset.   I engineered custom metrics, performed funnel and retention analysis, and created a dashboard-ready set of visualizations to simulate a real-world data analytics workflow at a PLG-focused company.

## 🔹 Dataset
- **Source:** Kaggle (Mobile App Usage Dataset)
- **Rows:** ~10,000 users  
- **Features:**  
  - Device & OS: `Device Model`, `Operating System`  
  - Usage: `App Usage Time`, `Screen On Time`, `Battery Drain`, `Data Usage`, `Number of Apps Installed`  
  - Demographics: `Age`, `Gender`  
  - Engagement Labels: `User Behavior Class`  

## 🔹 Key Metrics
| Metric                  | Definition |
|-------------------------|-----------|
| **Activation**          | App usage ≥ 30 minutes/day |
| **Engagement**          | App usage ≥ 2 hours/day + ≥50 installed apps |
| **Retention**           | Behavior Class ≥ 4 |
| **Engagement Index**    | Normalized score from usage, screen time, and battery drain |

## 🔹 Analysis Highlights

1. **Funnel Analysis**
   - Stages: Total Users → Activated → Engaged → Retained
   - Identifies where users drop off in the product journey.

![Funnel Chart](funnel_chart.png)

<img width="698" height="470" alt="image" src="https://github.com/user-attachments/assets/272c8368-eacf-4f65-a219-0a2f9a85791b" />


2. **Retention Curve**
   - Simulated Day 1–30 retention rates by `Behavior Class`.

![Retention Curve](retention_curve.png)

---

3. **Engagement Index Distribution**
   - Visualizes power users vs. casual users.

![Engagement Distribution](engagement_distribution.png)

---

4. **Segment Heatmap**
   - Compares engagement by OS and Gender.

![Segment Heatmap](segment_heatmap.png)

---

## 🔹 Key Insights
- **Retention Drivers:**  
  - Users in Behavior Class 4–5 retain **3× longer** than those in Class 1–2.  
- **OS Insights:**  
  - Android users showed slightly higher engagement than iOS users.  
- **Onboarding Gap:**  
  - Activation rate (~60%) indicates a need for improved onboarding flows.

---

## 🔹 Tools Used
- **Python**: Pandas, NumPy  
- **Visualization**: Matplotlib, Seaborn  
- **Data Source**: Kaggle Open Dataset  
- **Output**: Dashboard-ready CSV + Visualizations

