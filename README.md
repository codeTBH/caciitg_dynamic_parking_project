# caciitg_dynamic_parking_project
capstone project on dynamic parking price:
# 🚗 Dynamic Parking Lot Pricing System

This project simulates a real-time dynamic pricing engine for urban parking lots using Python, Bokeh, and Pathway. It implements and visualizes three pricing strategies—baseline, demand-based, and competitive—while comparing them against simulated competitor prices.

---

## 📊 Features

- **Real-time simulation** of parking lot data using Pathway
- **Three pricing models**:
  - **Model 1**: Baseline linear pricing based on occupancy
  - **Model 2**: Demand-based pricing using traffic, queue length, vehicle type, and special day indicators
  - **Model 3**: Competitive pricing that undercuts nearby competitors
- **Interactive Bokeh dashboard** for visualizing price evolution per lot
- **Streaming data** from a preprocessed CSV file to mimic live updates

---

## 🧠 Pricing Models

| Model | Description |
|-------|-------------|
| **Model 1** | Linear increase in price with occupancy |
| **Model 2** | Weighted demand score based on multiple real-world factors |
| **Model 3** | Adjusts price based on competitor pricing and lot fullness |

---

## 🛠️ Tech Stack

- **Python** (pandas, numpy)
- **Bokeh** for interactive visualization
- **Pathway** for real-time data streaming
- **Geopy** for optional distance-based competition logic

---

## 📁 Files

- `caiitg_parking_pricing.ipynb`: Main notebook with all models and visualizations
- `dataset.csv`: Input dataset containing timestamped parking lot data
- `parking_stream.csv`: Preprocessed stream-ready data

---

## 🚀 How to Run

1. Clone the repository and open the notebook in Google Colab or Jupyter.
2. Install dependencies:
   ```bash
   pip install pathway bokeh geopy
