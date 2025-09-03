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
This funnel visualizes the user journey through three **Product-Led Growth (PLG)** stages:

| Funnel Stage    | Approx. Users | Conversion |
|-----------------|--------------|------------|
| Total Users     | ~700         | 100%       |
| Activated       | ~640         | ~90%       |
| Engaged         | ~410         | ~64% of Activated |
| Retained        | ~275         | ~67% of Engaged |

### 🔍 Insights
1. **Strong Activation:** Onboarding is working well—most users reach activation.  
2. **Engagement Bottleneck:** The **largest drop** happens between Activation → Engagement (~36% loss).  
3. **Retention Strength:** Users who engage with core features have a **67% retention rate**, indicating that feature adoption correlates with stickiness.  
4. **Strategic Focus:** Improving feature discovery, nudges, and onboarding beyond activation could dramatically lift retention.


2. **Retention Curve**
   - Simulated Day 1–30 retention rates by `Behavior Class`.

![Retention Curve](retention_curve.png)
<img width="855" height="470" alt="image" src="https://github.com/user-attachments/assets/f5c20287-9ac5-46d9-859a-4400ddb96c48" />
This 30-day retention curve shows how user activity drops over time:

| Day | Retention Rate (Approx.) |
|-----|--------------------------|
| Day 1 | ~40% |
| Day 10 | ~25% |
| Day 30 | ~10% |

### 🔍 Insights
1. **Early Drop-Off:** Most churn occurs in the **first 7–10 days** after signup.  
2. **Steady Core Users:** After Day 10, retention decline slows; users who stay past this point are **more likely to become long-term users**.  
3. **Growth Focus:** Improving early onboarding, habit formation, and feature discovery could significantly lift retention rates.  
3. **Engagement Index Distribution**
   - Visualizes power users vs. casual users.

![Engagement Distribution](engagement_distribution.png)

<img width="571" height="455" alt="image" src="https://github.com/user-attachments/assets/6ecd5946-4c07-4611-b665-b81ff19f0edf" />
The Engagement Index condenses multiple activity metrics into a single score (0–1), making it easier to analyze user behavior patterns.

### 🔍 Insights
- **Bimodal Distribution:** Most users cluster at the **low** or **high** end of engagement.  
- **Low-Engagement Majority:** Many users are lightly engaged; these are likely **churn candidates**.  
- **Power User Segment:** High engagement cluster shows a **core loyal user base** worth prioritizing.  
- **Actionable Next Steps:**
  - Use engagement tiers for **targeted retention campaigns**.
  - Feed the index into the **churn prediction model** for better accuracy.

4. **Segment Heatmap**
   - Compares engagement by OS and Gender.

![Segment Heatmap](segment_heatmap.png)

<img width="846" height="470" alt="image" src="https://github.com/user-attachments/assets/e547f80e-e4e2-44a0-996f-f6d00798da52" />
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

