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
3. Run all cells to:

   - ✅ Preprocess the dataset  
   - 🚦 Simulate real-time pricing  
   - 📊 Visualize all three models in a live dashboard
---
## 📌 Example Output

The dashboard displays:

- **Solid lines**: Demand-based pricing (**Model 2**)
- **Dotted lines**: Competitive pricing (**Model 3**)
- **Dot-dashed lines**: Baseline pricing (**Model 1**)
- **Dashed lines**: Simulated competitor prices
## 🧱 Architecture Diagram

```mermaid
flowchart TD
    A[CSV Dataset] --> B[Preprocessing with pandas]
    B --> C[Real-time stream via Pathway]
    C --> D[Pricing Models]
    D --> D1[Model 1: Baseline]
    D --> D2[Model 2: Demand-based]
    D --> D3[Model 3: Competitive]
    D1 --> E[Price Output]
    D2 --> E
    D3 --> E
    E --> F[Bokeh Dashboard]


> ✅ GitHub will automatically render this Mermaid diagram when you save.

---

#### 🧠 Step 2: Add the Project Architecture & Workflow Explanation

1. Directly below the diagram, paste this:

```markdown
## 🧠 Project Architecture & Workflow

1. **Data Ingestion**  
   - Raw parking lot data is loaded from `dataset.csv`
   - Timestamps are parsed and features like occupancy rate, vehicle weight, and special day flags are engineered

2. **Real-Time Simulation**  
   - The dataset is streamed using **Pathway** to simulate live updates
   - A separate CSV (`parking_stream.csv`) is used for streaming into the dashboard

3. **Pricing Models**  
   - **Model 1**: Linear pricing based on occupancy
   - **Model 2**: Demand-based pricing using weighted features
   - **Model 3**: Competitive pricing that adjusts based on nearby lots

4. **Visualization**  
   - A **Bokeh dashboard** displays all three models and competitor prices in real time
   - Each lot is color-coded and supports interactive legend toggling

5. **Deployment-Ready**  
   - The notebook can be run in Google Colab or Jupyter
   - All dependencies are listed and installable via pip
