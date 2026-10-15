# Aqua-Roof
🛰️ Aqua Roof — Geospatial Rain Analytics: An interactive rooftop rainwater harvesting and groundwater recharge estimator built with satellite roof tracing, live climate data, and CGWB engineering formulas.
# 🛰️ Aqua Roof — Geospacial Rain Analytics
**Stop Guessing. Measure Your Roof from Space and Plan Your Rainwater Harvest in 60 Seconds.**

## 📌 Problem Statement
Many households and campuses could save thousands of liters of water and recharge depleted groundwater tables, but they do not know how much rainwater their roof can actually collect. Setup decisions for storage tanks and recharge pits are usually made by guesswork, leading to overflowing pits during heavy monsoons or wasted money on oversized structures.

## 💡 Our Solution
**Aqua Roof — Geospacial Rain Analytics** is a zero-setup, browser-based web tool that lets homeowners, Resident Welfare Associations (RWAs), and campus engineers:
1. **Trace & Resize Roofs on Satellite Imagery:** Click 3 or more corners of any building roof on high-resolution satellite maps (and drag the numbered corner points to adjust the shape) to compute the exact horizontal roof area in **sq. m ($\text{m}^2$)** and **sq. ft.**
2. **Locate Any Property Precisely:** Search by locality name, enter exact **Latitude & Longitude** coordinates, or use the multi-stage **GPS + Network Locator**.
3. **Calculate Honest Water Potential (CGWB Formula):** Computes Gross Rainfall and transparently subtracts surface evaporation loss, first-flush dirt diversion ($1.5\text{ mm}$ per rainy day), and filter loss.
4. **Plan Groundwater Recharge & Savings:** Recommends practical recharge pit dimensions (in meters and feet) based on a $50\text{ mm}$ heavy storm event and local soil type, alongside a visual **CGWB Filter Cross-Section Blueprint** and **5,000L water tanker payback calculation**.

---

## 🧮 Scientific Formula Used (CGWB Manual)
Since $1\text{ mm}$ of rainfall on $1\text{ m}^2$ of horizontal roof area equals exactly **1 Liter** of water:

$$\text{Gross Rainwater (L)} = \text{Horizontal Roof Area (m}^2\text{)} \times \text{Annual Rainfall (mm)}$$

$$\text{Net Collectable Water (L)} = \big[(\text{Area} \times \text{Rainfall} \times C) - \text{First-Flush Loss}\big] \times \text{Filter Efficiency}$$

* **Runoff Coefficient ($C$):** Concrete/RCC = `0.70` | Tiled Roof = `0.75` | Metal/GI Sheet = `0.90` | Brick Terrace = `0.60`
* **First-Flush Loss:** $1.5\text{ mm}$ per rainy day diverted to wash dust and debris off the roof.
* **Filter Efficiency:** `90%` standard sand-gravel filter recovery.

---

## 🛠️ Technology Stack
* **Frontend:** HTML5, CSS3 (Responsive Grid & Print-to-PDF Report Stylesheet), Vanilla JavaScript (ES6)
* **Geospatial & Mapping:** Leaflet.js, Esri World Imagery HD + Hybrid Labels, Google Satellite Hybrid, Esri/OpenStreetMap Street View, Spherical Shoelace Geodesic Area Algorithm
* **Climate & Location APIs:** Open-Meteo Historical Weather Archive API, OpenStreetMap Nominatim Geocoding, GeoJS / IPAPI Network Geolocation Fallback

---

## 🚀 How to Run Locally
1. Clone or download this repository.
2. Open `index.html` directly in **Google Chrome**, **Microsoft Edge**, or **Mozilla Firefox** (or launch via PyCharm's built-in browser preview).
