# ShadowLog: AI-Powered SIEM & Anomaly Detection

![License](https://img.shields.io/badge/license-MIT-blue.svg) ![Python](https://img.shields.io/badge/Python-3.10%2B-blue) ![Status](https://img.shields.io/badge/Status-Production%20Ready-green)

> **A lightweight, next-gen Security Information and Event Management (SIEM) system that uses Machine Learning to detect anomalies and reduce alert fatigue.**

## 🛑 The Problem
Traditional SIEMs generate thousands of alerts per day, causing "Alert Fatigue" for SOC teams. Most of these are false positives or noise.

## 🛡️ The Solution: ShadowLog
ShadowLog ingests logs from distributed systems, normalizes them into a common schema, and uses a **heuristic analysis engine** to flag only statistically significant anomalies.

### Key Features
* **Log Normalization:** Ingests JSON, Syslog, and CSV logs and converts them to a unified format.
* **Heuristic Anomaly Detection:** Uses statistical deviations (Z-score analysis) to detect unusual login times, data spikes, or unauthorized access attempts.
* **Real-Time Dashboard:** Visualizes threat levels and active incidents.
* **Reduced Noise:** Clusters related events to reduce alert volume by up to 80%.

## 🏗️ Architecture
1.  **Ingestion Layer:** Python-based collectors (Agents) running on endpoints.
2.  **Processing Layer:** Normalization and enrichment pipeline.
3.  **Analysis Layer:** ML model (Scikit-Learn/Custom Heuristics) to score events.
4.  **Presentation:** Streamlit/Flask dashboard.

## 🚀 Quick Start

### Prerequisites
* Python 3.10+
* Docker (Optional)

### Installation
```bash
# Clone the repository
git clone [https://github.com/YourUsername/ShadowLog.git](https://github.com/YourUsername/ShadowLog.git)

# Install dependencies
pip install -r requirements.txt

# Run the ingestion engine
python src/ingestor.py

# Launch the dashboard
streamlit run src/dashboard.py
