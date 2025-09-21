# ⚡ Edge-AI Powered Smart Energy Anomaly Detector  

**Microwatt Momentum Challenge 2025**  
Custom DSP + Neural-Net Accelerator for Smart Energy Systems  

---

## 📌 Overview  
This project integrates a **Smart Energy Anomaly Detector** with the open-source **Microwatt POWER CPU core**.  

- **DSP Pre-processing (Microwatt software):** Extracts key features from power waveforms (RMS, Crest Factor, Total Harmonic Distortion).  
- **Edge AI Accelerator (custom RTL):** A lightweight neural network (MLP) that classifies anomalies into *Normal, Spike, Noise, or Harmonic Distortion*.  
- **End-to-End Flow:** Simulated signals → DSP features → AI Accelerator → Classification → Logged + Visualized.  

The design is **SKY130-compatible**, reproducible in simulation, and demonstrates how **Edge AI + DSP** can improve power quality monitoring for **smart grids, IoT, and industrial systems**.  

---

## 🚀 Motivation & Use Cases  

### Why This Matters  
Modern power systems face challenges like **voltage spikes, harmonic distortion, and noisy loads**. Detecting these anomalies **in real time at the edge**:  
- Prevents equipment damage.  
- Improves grid efficiency.  
- Reduces downtime in factories.  
- Enhances safety in homes and IoT devices.  

### Real-World Applications  
- **⚡ Smart Grids:** Smart meters with local anomaly detection → early fault detection before blackouts.  
- **🏭 Industrial Maintenance:** Detects abnormal motor/pump signatures → enables predictive maintenance.  
- **🏠 IoT & Consumer Safety:** Prevents fire hazards by shutting down faulty appliances immediately.  
- **🔋 Renewables & EV Charging:** Detects harmonics and surges in inverters/chargers → protects electronics.  

---

## 🛠️ Technical Approach  

**System Flow:**  


**Key Components:**  
- **Microwatt CPU:** Runs software to compute RMS, Crest Factor, THD.  
- **Neural-Net Accelerator (RTL, Verilog/VHDL):** Implements a quantized MLP (int8 weights, int16 accumulators).  
- **Driver Software (C):** Loads weights, manages accelerator, retrieves outputs.  
- **Python Toolchain:**  
  - Generates synthetic waveforms (normal + anomalies).  
  - Trains & quantizes NN model.  
  - Provides golden reference for verification.  
  - Visualizes results (plots).  

---

## 📊 Features  
- DSP features: **RMS, Crest Factor, THD**.  
- Lightweight MLP accelerator (hidden layer + ReLU).  
- Streaming mode: sliding window anomaly detection.  
- Python verification with golden model.  
- SKY130-compatible RTL design.  

---

## 📅 Development Timeline  

| Week | Tasks |
|------|-------|
| **1** | Dataset generation, NN training + quantization, interface spec |
| **2** | RTL core blocks (MAC, ReLU, weight storage), unit tests |
| **3** | Integrate MLP, verify inference vs. Python golden model |
| **4** | DSP feature extraction in Microwatt, connect end-to-end |
| **5** | Streaming pipeline (sliding window), visualization of anomalies |
| **6** | Final polish: performance analysis, docs, demo video |

---

## ✅ Success Criteria  
- ≥90% classification accuracy on test signals.  
- ≥5× faster classification vs. CPU-only baseline.  
- End-to-end real-time simulation demo.  
- Fully reproducible repo (scripts + testbenches).  

---

## 📈 Impact  
By combining **classic DSP** with **Edge AI acceleration**, this project provides a **low-cost, scalable, and practical solution** for real-time anomaly detection in energy systems. It is designed to be reproducible, SKY130-compatible, and aligned with the goals of the **Microwatt Momentum Challenge 2025**.  
