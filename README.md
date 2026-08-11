# Spatial Network Performance Dashboards

Interactive dashboards for analysing, visualising and communicating spatial network performance.

Using a realistic synthetic cellular drive-test dataset, this project explores network coverage, service quality and performance across multiple frequency bands. Interactive dashboards support spatial exploration, service-target evaluation and identification of potential coverage gaps.

---

# Live Demo

Explore multiple performance metrics, compare frequency bands and evaluate service targets directly within your browser. The dashboards are published using **GitHub Pages** and can be explored directly in a web browser.

**Live application:**
**https://michael-slota.github.io/spatial-network-performance-dashboards/**

No installation or Python environment is required.

![Demo Dashboard](images/live_demo.png)

---

# Key Questions Answered

The dashboards are designed to support questions such as:

* Where does network performance fall below service targets?
* Which frequency bands provide the best coverage?
* How does network performance change with distance?
* Which areas would benefit most from additional infrastructure?
  
---

# Project Overview

Modern telecommunications networks generate large volumes of spatial performance data that can be difficult to interpret using traditional reports or spreadsheets.

This project demonstrates how interactive dashboards can be used to:

* explore network performance spatially,
* compare multiple radio-frequency bands,
* evaluate service-level compliance,
* identify coverage gaps,
* communicate engineering insights through intuitive visualisations.

The synthetic network represents a city served by eight 5G macro-cell towers with measurements collected throughout the surrounding area.

The simulated environment includes:

* eight central macro-cell towers,
* four operating frequency bands,
* a directional repeater improving higher-frequency performance,
* a localised dead zone,
* realistic distance-dependent propagation,
* correlated spatial variation,
* measurement noise,
* multiple network performance metrics.

---

# Network Performance Metrics

Each measurement contains the following indicators.

| Metric                  | Description                                         |
| ----------------------- | --------------------------------------------------- |
| **RSRP**                | Reference Signal Received Power (coverage strength) |
| **RSRQ**                | Reference Signal Received Quality                   |
| **SINR**                | Signal-to-Interference-plus-Noise Ratio             |
| **Download Throughput** | User download performance                           |
| **Upload Throughput**   | User upload performance                             |
| **Latency**             | Network response time                               |
| **Packet Loss**         | Reliability of packet delivery                      |

---

# Dashboard Preview

## Distance Performance Dashboard

![Distance Dashboard](images/distance_dashboard.png)

The distance dashboard explores how each performance metric changes as measurements move away from the central tower cluster. Interactive controls allow users to compare frequency bands, evaluate service targets and estimate coverage limits.

---

## Directional Coverage Dashboard

![Directional Dashboard](images/direction_dashboard.png)

The directional dashboard summarises network performance using polar sectors and distance rings, highlighting directional trends and areas requiring further investigation.

---

# Dashboard Features

The dashboard suite includes:

* Interactive Plotly visualisations
* Frequency-band comparison
* Distance-decay analysis
* Directional performance analysis
* Service-target evaluation
* Interactive filtering
* Hover tooltips
* Summary statistics
* Coverage estimation
* Standalone HTML deployment

---

# Service Targets

The dashboards compare every measurement against predefined engineering targets.

## Target Performance

| Metric              | Target     |
| ------------------- | ---------- |
| RSRP                | ≥ -95 dBm  |
| RSRQ                | ≥ -10 dB   |
| SINR                | ≥ 15 dB    |
| Download Throughput | ≥ 100 Mbps |
| Upload Throughput   | ≥ 20 Mbps  |
| Latency             | ≤ 30 ms    |
| Packet Loss         | ≤ 1%       |

## Minimum Acceptable Performance

| Metric              | Threshold  |
| ------------------- | ---------- |
| RSRP                | ≥ -105 dBm |
| RSRQ                | ≥ -14 dB   |
| SINR                | ≥ 5 dB     |
| Download Throughput | ≥ 25 Mbps  |
| Upload Throughput   | ≥ 5 Mbps   |
| Latency             | ≤ 60 ms    |
| Packet Loss         | ≤ 3%       |

These thresholds allow the dashboards to estimate service compliance across both distance and direction.

---

# Repository Structure

```text
index.html
data/
    dashboards/
    supporting/
images/
README.md
```

---

# Analytical Workflow

```text
Synthetic network measurements
          ↓
Quality assurance
          ↓
Spatial analysis
          ↓
Service target evaluation
          ↓
Coverage estimation
          ↓
Interactive Plotly dashboards
          ↓
GitHub Pages deployment
```

Although this repository focuses on the finished dashboards, every visualisation originates from a single reproducible analytical workflow to ensure consistency across the application.

---

# Technologies

* Python
* pandas
* NumPy
* SciPy
* Plotly
* HTML
* GitHub Pages

The dashboards are exported as standalone HTML applications and execute entirely within the browser.

---

# Limitations

The measurements used throughout this project are synthetic but were designed to resemble realistic cellular drive-test surveys. The emphasis is therefore on demonstrating analytical techniques, spatial visualisation and stakeholder communication rather than representing an operational mobile network.
