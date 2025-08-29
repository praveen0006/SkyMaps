# Flying Vehicle Route Map (QGIS + Leaflet)

This project demonstrates how to build an **interactive route map for future flying vehicles (drones, air taxis, flying cars, etc.)** using **QGIS** and publishing it with **Leaflet (qgis2web export)**.

---

## 🚀 Project Overview

* Designed for **Telangana (India)** as a pilot region.
* Integrates **terrain (DEM)**, **buildings**, and **custom drone/air-taxi routes**.
* Generates an interactive web map where users can view routes, obstacles, and infrastructure.
* Exported from **QGIS 3.40.9 (Bratislava)** using **qgis2web**.

---

## 📂 Project Structure

```
project/
│-- index.html               # Main web map (open this in a browser)
│-- css/                     # Stylesheets for map UI
│-- js/                      # Leaflet + plugins
│-- data/                    # GeoJSON layers exported from QGIS
│   ├── Drone_Routes_0.js
│   ├── Drone_Path_7.js
│   ├── building_2.js
│   ├── Woxsen_Buildings_3.js
│   ├── woxsen_buildings_6.js
│-- images/ (optional)       # Any icons or logos
```

---

## 🗺️ Layers Included

1. **Drone Routes** – predefined air corridors.
2. **Drone Path** – generated safe paths with attributes (altitude, length).
3. **Buildings** – imported from OSM (with height attributes where available).
4. **Woxsen Buildings** – additional test building datasets.
5. **Base Maps** – OpenStreetMap + Google Satellite.

---

## ⚙️ Setup Instructions

### 1. Local Preview

To view the map locally:

1. Download the project folder.
2. Use a local web server (because Leaflet needs `http://` to load data).

   ```bash
   # Python 3
   python -m http.server 8080
   ```
3. Open in browser:

   ```
   http://localhost:8080/index.html
   ```

### 2. Public Hosting

Options to share publicly:

* **GitHub Pages** → Upload the folder to a GitHub repo → enable Pages → access via `<username>.github.io/<repo>`
* **Netlify / Vercel** → Drag & drop folder for free hosting
* **Any static web host** (Apache/Nginx/S3/Cloudflare Pages)

---

## 📌 Next Steps / Improvements

* ✅ Add **routing algorithm** (shortest path avoiding buildings + terrain).
* ✅ Add **public input search bar** for origin/destination.
* ✅ Show **obstacle heights (DEM + buildings)** in 3D view.
* ⏳ Integrate **flight regulations (no-fly zones, altitude limits)**.
* ⏳ Scale from **city-level demo → Telangana state-wide platform**.

---

## 🛠️ Tools Used

* **QGIS 3.40.9** – data preparation & styling
* **qgis2web** – export to Leaflet
* **Leaflet.js** – interactive web map framework
* **OpenStreetMap / Google Satellite** – basemaps

---

## 👥 Author

Developed by **Praveen Kumar** as a prototype for **future flying vehicle route mapping**.

---

## 📄 License

This project is open-source for research and educational purposes.
