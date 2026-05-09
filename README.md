🌊 S.A.F.A.L: Smart Aqua Flood Alert Layer

🤖 A Machine Learning System for Urban Waterlogging Prediction

Author: Kshitij Chauhan

Domain: Machine Learning · Urban Systems · Environmental Modeling

Type: Research Prototype (INSPIRE-MANAK State Qualifier Project)

📝 Overview

Urban flooding is not just rainfall — it is a systems failure involving saturation, drainage limits, and time-dependent accumulation. 🏗️

S.A.F.A.L explores whether long-term meteorological data can be used to predict waterlogging risk before system breakdown occurs. This project is an experimental attempt to model flooding as a temporal, state-dependent system, rather than a single-event prediction problem. 📉

💡 Key Idea

Flood risk is not determined by today’s rain — but by how much water the system has already absorbed over time. 💧

The Core Concept:

7-day rainfall history matters more than single-day rainfall intensity.

Urban flooding behaves like a memory-based system. 🧠

🏗️ System Architecture

1. Data Layer 📊

32 years of Safdarjung (IMD) meteorological data (1990–2022).

Features: Rainfall, Humidity, Temperature.

2. Feature Engineering Layer ⚙️

7-day rolling rainfall: Acts as a soil saturation proxy.

Rainfall intensity spikes: Captures abrupt gradients.

Cumulative moisture tracking: Models the "state" of the environment.

3. Prediction Layer 🤖

Linear Regression: Baseline for correlation.

Random Forest: Used for feature importance and non-linear patterns.

Sequence-weighted temporal model: Prioritizes recent history (Best Performance 🏆).

4. Response Layer (Conceptual) 🚨

Flood-risk scoring system.

Automated drainage trigger logic.

120-second stabilization delay: To prevent oscillation (Pump Chatter control).

✨ Key Results

❌ Linear models failed during monsoon spikes (non-linear limitation).

✅ Random Forest improved stability and feature detection.

🌟 Temporal weighted model performed best for flood-event recall.

Main Insight: Temporal accumulation is the strongest predictor of urban flooding.

🧠 Engineering Insight

Traditional models assume: Rainfall events are independent.

S.A.F.A.L shows: Flooding is state-dependent and system memory is critical. 🔄

🚧 Limitations

No real-time IoT sensor data (yet). 📡

No drainage network topology modeling.

Daily dataset cannot capture flash flood dynamics.

Infrastructural conditions (blockages) are not included.

🛠️ Technologies Used

Language: Python 🐍

Libraries: Pandas, NumPy, Scikit-learn, Matplotlib

Frameworks: TensorFlow (experimental)

🔮 Research Direction

Future extensions:

🌐 IoT-based drainage monitoring.

🕸️ Graph-based city drainage modeling.

🤖 Reinforcement learning for flood response.

📡 Real-time rainfall radar integration.

🏁 Project Status

Stage: Experimental Research Prototype

Level: State-level INSPIRE-MANAK Qualified Project 🏅

📚 References & Links

GitHub Repository: S.A.F.A.L — Source Code 💻

Project Website: Explore S.A.F.A.L 🌍

Paper: Full technical documentation available in docs/research_paper.pdf.

📜 License

MIT License — Open for academic and research use.
