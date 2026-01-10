# Beyond Passenger Numbers  
## Hidden Connectivity in the Global Airline Network

**MSc Data Science Project – Birkbeck, University of London**  
Supervisor: Dr Felix Reidl  

---

## 📌 Project Overview

Airports are usually ranked by **passenger volume or number of flights**.  
This project asks a different, more structural question:

> **Which airports are truly important to the global airline network – and why?**

Using **network theory + geospatial analysis**, I show that airport importance is **multi-dimensional** and depends on *how* an airport connects the network, not just how busy it is.

---

## 🎯 Why This Project Matters

Traditional rankings miss important insights:

- Some airports **bridge continents**
- Some **connect influential hubs**
- Some **dramatically reduce travel distance** for entire regions

This project demonstrates why **no single metric** (like passenger numbers) is enough.

---

## 🔍 What Makes This Project Different

- Models the airline system as a **directed, distance-weighted network**
- Uses **multiple centrality measures together**, not in isolation
- Incorporates **real geographic distance** (Haversine formula)
- **Mathematically explains unexpected results**
- Shows why **small regional airports can outrank global hubs** under certain metrics

---

## 🧠 Methodology (High Level)

**Data**
- OpenFlights global airport & route dataset
- ~3,200 airports, ~36,000 routes

**Network Construction**
- Nodes: airports  
- Edges: directed flight routes  
- Edge weights: geographic distance (km)

**Centrality Measures Used**
- **Degree** – number of direct connections  
- **Betweenness** – importance as a bridge between regions  
- **Eigenvector** – connection to influential hubs  
- **Harmonic** – overall travel efficiency (distance-based)

---

## ⭐ Key Findings (With Real Insight)

### 1️⃣ Major hubs dominate Degree centrality  
Airports like **Frankfurt, Paris CDG, Amsterdam** lead due to broad route diversity.

---

### 2️⃣ Strategic connectors dominate Betweenness  
Airports such as **Keflavik (Iceland)** and **Anchorage** rank highly despite modest traffic, because they sit between major regions.

---

### 3️⃣ Influence matters more than volume (Eigenvector)  
**Heathrow, JFK, Dubai** score highly because they connect to *other powerful hubs*, even if they don’t have the most routes.

---

### 4️⃣ Small airports can dominate efficiency (Harmonic)  
Tiny airports like **Papa Westray and Westray (Orkney Islands)** top Harmonic centrality.

**Why?**
- Extremely short flight distances (e.g. 2.8 km)
- Harmonic centrality sums inverse distances
- Short links produce very large efficiency gains

This result is **mathematically proven** in the analysis and not an anomaly.

---
## 🧮 Example: Why Papa Westray Ranks So High (Harmonic Centrality)

Harmonic centrality measures **how efficiently an airport can reach all others** by
summing the inverse of travel distances.

In simple terms:

- **Short distances contribute a lot**
- **Long distances contribute very little**

### How the math works (intuitive explanation)

- A **2.8 km** flight contributes approximately **0.36**
- A **400 km** flight contributes approximately **0.0025**

Even though both are just one connection, the shorter flight contributes **over 140× more**.

### Why this matters

Papa Westray has **very short connections** to nearby islands.
These short distances **compound**, giving it an extremely high efficiency score.

➡️ **Local proximity compounds efficiency**, even with very few flights.
---

## 🗺️ Visual Outputs

- Global airport maps by centrality
- Correlation heatmaps between measures
- Ranked top-10 airports for each metric

📌 *Image placeholders below (to be added)*  
---

## 🛠️ Tools & Technologies

- **Python**
- **NetworkX**
- **Pandas / NumPy**
- **GeoPandas / Shapely**
- **Matplotlib / Seaborn**
- **Haversine distance**

---

## 📁 Repository Structure
global-airline-network-centrality/
│
├── README.md
├── Netwrork_Aanalsis.ipynb
├── data/
│   ├── nodes.csv
│   ├── edges.csv
│   └── gprops.csv
├── report/
│   └── MSc_Dissertation.pdf
└── images/
---

## 🎓 Academic Context

This project was submitted as part of the **MSc Data Science** degree at  
**Birkbeck, University of London**, and demonstrates applied:

- Network science
- Geospatial analysis
- Mathematical reasoning
- Real-world interpretation

---

## 📬 Contact

**Mohd Nafees**  
📍 London, UK  
🔗 LinkedIn: https://linkedin.com/in/mohd-nafees-59863524b  
💻 GitHub: https://github.com/Combatant94
