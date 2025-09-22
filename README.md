# ⚡ Project Proposal: Edge-AI Powered Smart Energy Anomaly Detector

**Microwatt Momentum Challenge 2025**  
Custom DSP + Neural-Net Accelerator showcasing Edge AI in energy anomaly detection  

---

## 📌 Overview  
This project demonstrates how **Edge AI** can bring intelligence directly into embedded systems by combining a **Microwatt POWER CPU** with a **custom neural-net accelerator**.  

As a proof of concept, we will implement a **Smart Energy Anomaly Detector**:  
- **DSP Pre-processing:** Extracts key signal features (RMS, Crest Factor, THD).  
- **Edge AI Accelerator:** A quantized neural network (MLP) classifies anomalies into *Normal, Spike, Noise, or Harmonic Distortion*.  
- **End-to-End Flow:** Simulated signals → DSP features → AI Accelerator → Classification → Logged + Visualized.  

---

## 🚀 Motivation  

The core motivation of this project is to explore and showcase the **power of Edge AI**:  
- Traditional systems rely on **cloud-based analytics** or **simple DSP thresholds**, which are either too slow, too costly, or too limited.  
- By moving **AI inference directly to the edge**, devices become **faster, smarter, and autonomous**.  
- The **Microwatt core + AI accelerator** combination provides a lightweight, open-source platform to demonstrate this vision.  

We chose **Smart Energy anomaly detection** as the demonstration use case because:  
- It’s highly relevant (spikes, distortion, noise in power systems).  
- It showcases how AI can distinguish **subtle, nonlinear patterns** that DSP alone cannot.  
- It connects to real-world needs in **smart grids, IoT safety, renewable energy, and industrial systems**.  

---

## 🛠️ Technical Approach  


**Key Components:**  
- **Microwatt CPU:** Runs software to compute RMS, Crest Factor, THD.  
- **Neural-Net Accelerator:** Implements a quantized MLP (int8 weights, int16 accumulators).  
- **Driver Software:** Loads weights, manages accelerator, retrieves outputs.  
- **Python Toolchain:**  
  - Generates synthetic waveforms (normal + anomalies).  
  - Trains & quantizes NN model.  
  - Provides golden reference for verification.  
  - Visualizes results (plots).  

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

