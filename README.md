# MechIQ-MVP
# MechIQ: Hardware-Enabled SaaS for Industrial PdM

**Transforming legacy factory machinery into smart, self-diagnosing assets using Edge AI.**

## The MVP Showcase
Welcome to our digital data room. This repository contains the technical validation, edge-firmware architecture, and business case for our Predictive Maintenance (PdM) ecosystem.

* **[Simulation Link](https://wokwi.com/projects/469985754780072961)** 

---

## The Problem & Solution
Indian manufacturing is powered by legacy machines that lack digital data streams. Unplanned downtime costs millions, but pure SaaS solutions fail because the data simply doesn't exist on the factory floor. 

**Our Solution:** We retrofit "unsexy" legacy machines with low-cost ESP32-S3 sensor nodes. These nodes run embedded machine learning to detect anomalies locally, acting as a Trojan horse to capture data and fuel our highly scalable SaaS monitoring dashboard.

---

## Machine Learning Validation
We trained our **Isolation Forest** anomaly detection model on the industry-standard Case Western Reserve University (CWRU) bearing dataset. 

Our model operates identically to how it runs on our ESP32 edge nodes—extracting Time-Domain features (RMS, Kurtosis) and Frequency-Domain features (FFT bands) over a simulated 28-day baseline observation period.

![ML Validation Results](./assets/ML_Validation.png)
*Results: Achieved >85% detection rate on catastrophic faults while maintaining a <5% false alarm rate on normal baselines.*

---

## Edge Hardware Architecture
To ensure low latency and data privacy, the anomaly detection math happens directly on the machine. The raw high-frequency vibration data is processed locally, and only the "Health Score" is sent to the cloud.

![System Architecture](./assets/System_Architecture.png)
*Visual MVP: Sensor array topology mapped to the ESP32 microcontroller.*

---

## 📂 Repository Navigation
Dive deep into our codebase and algorithms:
- `/src/data_preprocessing.ipynb` - Python notebook proving the Isolation Forest logic.
- `/src/edge_firmware.ino` - The C++ firmware that calculates Kurtosis and FFTs on the edge.
- `/docs/Pitch_Deck.pdf` - The commercialization strategy and market sizing.

---
**Founder:** Yamuna
