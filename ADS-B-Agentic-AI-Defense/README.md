# Autonomous Agentic AI Framework for ADS-B Channel Security

## 🛰️ Project Overview
This repository hosts the research, development, and architectural design for an autonomous, real-time intrusion detection and mitigation system securing the **Automatic Dependent Surveillance-Broadcast (ADS-B)** flight channel. Developed at the **NCRA-UAV Lab (FAST-NUCES, Islamabad)**, this framework transitions traditional, passive anomaly detection into an active **Agentic Multi-Agent System**.

The primary objective is to detect, isolate, and mitigate malicious radio frequency (RF) exploits—specifically **GPS/Telemetry Spoofing, Signal Jamming, and Replay Attacks**—by employing a dynamic "Cross-Channelling" validation strategy.

---

## 🧠 Architectural Concept: Cross-Channelling Verification
Because the global 1090 MHz aviation broadcast channel lacks native encryption or cryptographic authentication, malicious actors can easily inject arbitrary packets. Our proposed framework utilizes a **Tri-Agent Orchestration Model** that treats independent validation systems as callable tools:

1. **Sensor Agent (High-Speed Ingestion):** Triage layer filtering incoming 1090 MHz Mode S telemetry streams at microsecond scales.
2. **Critic Agent (Multi-Source Cross-Check):** The cognitive core. Upon detecting statistical anomalies, it asynchronously triggers specialized verification sub-modules:
   * **Kinematic Validation:** Employs an Extended Kalman Filter (EKF) to cross-reference reported trajectories against physical aircraft performance envelopes.
   * **Spatial Triangulation:** Uses Time Difference of Arrival (TDoA) algorithms across multiple ground receivers to isolate the physical coordinate of the RF transmitter.
   * **RF Fingerprinting:** Analyzes raw physical IQ waveforms via Convolutional Neural Networks (CNNs) to verify hardware oscillator signatures.
3. **Actuator Agent (Autonomous Mitigation):** Policy engine that dynamically isolates corrupted data streams and recalculates secure alternative routing vectors for adjacent UAVs.

---

## 📁 Repository Directory Blueprint

* `/docs/research/`: Contains detailed technical literature reviews of the 5 assigned core research papers, focusing on mathematical models, extracted datasets, and architectural blind spots.
* `/docs/logs/`: Contains the continuous, timestamped engineering journals tracking daily progress, blockers encountered, and upcoming milestones for each team researcher.

---

## 👥 Research & Development Team: Vakin
* **Abdul Mannan** — AI/ML Intern, NCRA-UAV Lab (FAST-NUCES)
* **[Talha Anwar]** — AI/ML Intern, NCRA-UAV Lab (FAST-NUCES)

**Supervised By:** [Supervisor's Name/Designation]  
**Institution:** National Center of Robotics and Automation (NCRA) - UAV Lab, FAST-NUCES, Islamabad.