# Network Data Analysis – Coursework

This repository contains the full implementation and analysis for the **Network Data Analysis** coursework.  
The project applies graph theory, network science, and spatial analysis techniques to study both **social interaction networks** and **real-world spatial networks**, combining empirical analysis with simulation models and visualisation.

---

## 📌 Project Overview

The coursework is divided into two main parts:

1. **Social Network Analysis of Wikidata Editor Interactions**
2. **Spatial Network Analysis of a Road Network in Leeds**

Across both parts, real-world networks are constructed, analysed using standard network metrics, compared against random baselines, and explored through simulations and spatial statistics.

---

## 🧠 Part 1: Wikidata Editor Networks

### Network Construction
- Nodes represent **Wikidata users**
- Edges represent **interaction within the same page and discussion thread**
- Three networks analysed:
  - Request for Comments (RFC)
  - WikiProjects
  - Users network

Equivalent **random networks** were generated using the Erdős–Rényi model to enable structural comparison.

### Network Metrics
Each network was analysed using:
- Degree statistics (mean, median, distribution)
- Clustering coefficient
- Connected components
- Betweenness centrality
- Average shortest path length

These metrics were used to position networks along the **regular–small-world–random** spectrum.

### Diffusion Modelling
A **Threshold Model** was implemented to simulate behavioural propagation (e.g. controversial participation):
- Simulations run on both real and random networks
- Parameters tuned per network structure
- Diffusion speed and reach compared across networks
- Early-stage propagation used to identify at-risk nodes

This demonstrates how **network topology influences behavioural spread**.

---

## 🗺️ Part 2: Spatial Network Analysis (Leeds)

### Road Network Construction
- Road network extracted from **OpenStreetMap** using OSMnx
- Central Leeds region selected based on accident density
- Network simplified and analysed for planarity and connectivity

### Accident Analysis
- Traffic accident points snapped to the road network
- Spatial clustering examined using:
  - K-function
  - Moran’s I
- Analysis of accident proximity to intersections

### Voronoi-Based Route Planning
- Network-based Voronoi diagrams used to divide the city
- Marathon-length routes (~42km) generated within regions
- Demonstrates the interaction between **spatial structure and routing feasibility**

### Provenance Networks & Embeddings
- A fictional **PROV provenance graph** constructed
- PageRank applied to identify structurally important entities
- Knowledge graph embedding models (TransE, RotatE) trained and evaluated
- Limitations of applying embeddings to small graphs discussed

---

## 🛠️ Technologies Used

- **Python**
- **NetworkX**
- **NDLib**
- **OSMnx**
- **Folium**
- **PySAL / Spaghetti**
- **Matplotlib**
- **PyKEEN**

---
