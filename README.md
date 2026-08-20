# HydroSync AI: Dam Monitoring and Flood Prediction System

An AI-powered, virtualization-based dam monitoring and flood prediction system that simulates dam behavior and forecasts overflow risk **without relying on physical IoT sensors**. The system uses 10 years of historical dam records to train machine learning models, visualize trends, simulate dam operations in 3D, and send automated early-warning alerts to nearby villagers.

**Case Study:** Jayakwadi Dam, Maharashtra, India

---

## 🚀 Overview

Traditional dam monitoring systems depend heavily on costly, hard-to-maintain physical sensors and real-time IoT infrastructure. HydroSync AI addresses this gap with a **cost-effective, scalable, sensor-free approach** that uses historical rainfall, inflow, and water-level data to:

- Predict current/future year water conditions
- Identify high-risk overflow periods in advance
- Visualize dam and village locations for impact analysis
- Simulate dam gate operations in an interactive 3D model
- Trigger automated WhatsApp alerts when water levels cross critical thresholds

---

## ✨ Key Features

- **📊 Data Visualization Dashboard** — Interactive charts (inflow, outflow, rainfall, water level) with year/month/season filters, peak inflow/outflow stats, and surplus/deficit day tracking.
- **🗺️ Dam & Village Location Map** — Geographical view of the dam and surrounding villages to identify potentially affected areas.
- **🤖 AI-Based Prediction Engine** — Random Forest model trained on 10 years of historical data to forecast overflow risk and highlight high-risk months.
- **🧊 3D Dam Simulation** — Real-time 3D visualization of water flow, reservoir levels, and gate operations (open/close) with adjustable inflow and camera views.
- **📝 Villager Registration Portal** — Villagers register their village and mobile number to receive critical alerts.
- **📲 Automated WhatsApp Alerts** — Twilio-powered emergency notifications sent to registered numbers when water levels reach critical thresholds.

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Frontend** | Next.js (React) |
| **Backend** | Node.js |
| **Machine Learning** | Python, Pandas, NumPy, Scikit-learn (Random Forest) |
| **Database** | MongoDB |
| **Data Visualization** | Chart.js |
| **Alerts** | Twilio (WhatsApp API) |
| **APIs** | Weather/rainfall APIs |
| **Deployment** | Vercel / Render |
| **Version Control** | Git / GitHub |

---

## 📈 Model Performance

**Algorithm:** Random Forest Classifier
**Accuracy on Test Data:** **89.47%**

| Class | Precision | Recall | F1-score | Support |
|---|---|---|---|---|
| Safe (0) | 0.98 | 0.90 | 0.94 | 675 |
| Risk (1) | 0.41 | 0.80 | 0.54 | 56 |
| **Weighted Avg** | 0.94 | 0.89 | 0.91 | 731 |

The model prioritizes **recall over precision** for the "Risk" class — since this is a safety-critical system, correctly catching 80% of actual overflow events is more important than avoiding occasional false alarms.

---

## 🧩 System Architecture / Flow

```
Start → User Login → Dashboard
                        ├── Dam Location Page (map of dam + nearby villages)
                        ├── Visualization Page (10-year historical trends)
                        ├── 3D Model Page (dam simulation, gate control)
                        └── Prediction Page (AI-based overflow risk forecast)
```

## 🔄 Methodology

1. **Data Collection** — 10 years of dam data (rainfall via weather APIs; inflow, storage, water level, FRL, outflow from government portals).
2. **Data Preprocessing** — Missing water-level values filled via linear interpolation; feature engineering on rainfall, inflow, and storage variations.
3. **Model Training** — Random Forest trained to learn relationships between rainfall, inflow, and water levels.
4. **Model Evaluation** — Assessed using accuracy, precision, recall, and F1-score.
5. **Prediction** — Model takes month/expected rainfall as input and outputs overflow probability.
6. **Visualization** — Historical trends rendered as interactive charts.
7. **Alerting** — WhatsApp notifications triggered when predicted/simulated water level exceeds a defined threshold.

---

## 📦 Deliverables

1. Trained Random Forest prediction model with full data preprocessing pipeline
2. Interactive web dashboard for historical & predicted data visualization
3. 3D dam simulation with villager registration module
4. Automated WhatsApp early-warning alert system

---

## 🔮 Future Scope

- Integration with real-time weather APIs, rainfall sensors, and satellite data
- Advanced deep learning / hybrid AI models for improved long-term forecasting
- More realistic, physics-based 3D simulation
- Native mobile app for wider accessibility
- Multi-dam support for large-scale water resource management

---

## 👥 Contributors

- Suraj Barate
- Prathmesh Jadhav
- Harshad Sangde
- Chaitanya Thakare

**Guide:** Dr. Sujata Bhairnallykar
**Department of Computer Engineering, Saraswati College of Engineering, Kharghar** (Affiliated to University of Mumbai) — 2025–26

---

## 📄 License

This project was developed as an academic Bachelor of Engineering project. Please contact the contributors for reuse or collaboration inquiries.
