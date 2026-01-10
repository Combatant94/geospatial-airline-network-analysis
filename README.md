# ✈️ Beyond Passenger Numbers  
## Hidden Connectivity in the Global Airline Network  

**MSc Data Science Project – Birkbeck, University of London**  
**Supervisor:** Dr Felix Reidl  

<img width="2000" height="1336" alt="image" src="https://github.com/user-attachments/assets/3d2f4422-269a-4274-bfba-69be72325698" />


---

## 📌 Project Overview

Airports are usually ranked by passenger numbers or flight volume.  
While useful, these rankings answer only one question: **who is busy?**

This project asks a different and more structural question:

> **Which airports are genuinely important to the global airline network — and for what reason?**

By combining **network theory** with **real geographic distance**, this analysis shows that airport importance is **not one-dimensional**.

An airport can matter because it:
- connects many places  
- links regions  
- makes travel significantly more efficient — **even if it is small**

---

## 🎯 Why This Project Matters

Traditional rankings hide important roles played by airports:

- Some airports act as **bridges between continents**
- Some connect **highly influential hubs**
- Some dramatically **reduce travel distance** for entire regions

If we only look at passenger numbers, we miss these roles entirely.

This project demonstrates why **no single metric** can explain global connectivity.

---

## 🔍 What Makes This Project Different

This analysis goes beyond surface-level rankings:

- Models the airline system as a **directed, distance-weighted network**
- Uses **multiple centrality measures together**, not in isolation
- Incorporates **real geographic distance** using the Haversine formula
- Provides **mathematical justification** for unexpected results
- Explains why **small regional airports** can outrank global hubs under certain measures

Every result is explained by **how the metric works**, not treated as an anomaly.

---

## 🧠 Methodology (High Level)

### Data
- OpenFlights global airport and route dataset
- ~3,200 airports
- ~36,000 directed flight routes

### Network Construction
- **Nodes:** airports  
- **Edges:** directed flight routes  
- **Edge weights:** geographic distance (km)

This reflects how air travel actually works: **direction matters, and distance matters.**

### Centrality Measures Used
- **Degree** – how many direct connections an airport has  
- **Betweenness** – how often an airport lies on shortest paths between regions  
- **Eigenvector** – how connected an airport is to other influential airports  
- **Harmonic** – how efficiently an airport can reach all others (distance-based)

Each measure captures a **different role** in the network.

---

## ⭐ Key Findings (With Real Insight)

### 1️⃣ Major hubs dominate Degree centrality

Airports such as **Frankfurt**, **Paris CDG**, and **Amsterdam** rank highest because they serve a wide range of destinations.

Degree centrality rewards **route diversity**, which naturally favours large hubs.

---

### 2️⃣ Strategic connectors dominate Betweenness

Airports like **Keflavik (Iceland)** and **Anchorage** rank highly despite modest passenger traffic.

**Why?**  
Their geographic position places them on many shortest paths between regions.

They function as **bridges**, not just destinations.

---

### 3️⃣ Influence matters more than volume (Eigenvector)

**Heathrow**, **JFK**, and **Dubai** score highly because they are connected to other powerful hubs.

Eigenvector centrality does **not** reward how many routes you have —  
it rewards **who you are connected to**.

This explains why some globally important airports rank higher here than in simple route counts.

---

### 4️⃣ Small airports can dominate efficiency (Harmonic)

Tiny airports such as **Papa Westray** and **Westray** (Orkney Islands) rank at the very top of Harmonic centrality.

At first glance, this looks impossible — until you understand how the metric works.

---

## 🧮 Example: Why Papa Westray Ranks So High (Harmonic Centrality)

Harmonic centrality measures how efficiently a node can reach all others by summing inverse distances:

C_H(v) = Σ (1 / d(v, u))

### What this means in practice
- Short distances contribute **a lot**
- Long distances contribute **very little**

### Intuitive comparison
- A **2.8 km** flight contributes ≈ **0.36**
- A **400 km** flight contributes ≈ **0.0025**

These values come directly from inverse distance:
- `1 / 2.8 ≈ 0.36`
- `1 / 400 = 0.0025`

So although both are “one flight”, the short flight contributes **over 140× more** to efficiency.

### Why Papa Westray benefits

Papa Westray is connected by **extremely short flights** to nearby islands.  
Each short distance adds a large efficiency contribution, and together they compound.

Large hubs may have many connections, but those connections span **hundreds or thousands of kilometres**, producing very small inverse values.

➡️ **Local proximity compounds efficiency, even with very few flights.**

This result is **mathematically expected**, not an anomaly.

---

## 🗺️ Visual Outputs
- Global airport maps coloured by centrality measure
- Correlation heatmaps comparing metrics
- Top-10 ranked airports for each centrality

📌 Figures will be added in the `/images` directory.

---

## 🛠️ Tools & Technologies
- Python  
- NetworkX  
- Pandas / NumPy  
- GeoPandas / Shapely  
- Matplotlib / Seaborn  
- Haversine distance calculations  

---

## 📁 Repository Structure

```text
global-airline-network-centrality/
│
├── README.md
├── Network_Analysis.ipynb     Python-code
│
├── data/
│   ├── nodes.csv
│   ├── edges.csv
│   └── gprops.csv
│
├── report/
│   └── Centrality_metrics _airlines netwrok(1).pdf  Full_Report
│
└── images/
```

## 🎓 Academic Context

This project was submitted as part of the **MSc Data Science** degree at  
**Birkbeck, University of London**.

It demonstrates applied skills in:
- Network science
- Geospatial analysis
- Mathematical reasoning
- Translating theory into real-world insight

---

## 📬 Contact

**Mohd Nafees**  
📍 London, UK  
🔗 LinkedIn: https://linkedin.com/in/mohd-nafees-59863524b  
💻 GitHub: https://github.com/Combatant94  

---

*If you want next:*  
- 📌 image placement suggestions  
- 📌 a 10-second recruiter summary at the top  
- 📌 README optimisation for Snowfox / Leisure DB  

**Say the word.**
